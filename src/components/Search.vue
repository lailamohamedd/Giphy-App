<template>
  <!-- Start search -->
  <div class="search">
    <container>
      <!-- Start input-group -->
      <div class="input-group mb-3">
        <input
          placeholder="Type something to search for awesome gifs"
          v-model="keyword"
          @input="onInput"
          aria-label="Recipient's username"
          aria-describedby="button-addon2"
        />
        <button type="submit" class="btn btn-primary" id="button-addon2">
          <i @click="copyUrl" class="fa fa-search"></i>
        </button>
      </div>
      <!-- End input-group -->
    </container>
  </div>
  <!-- End search -->
</template>

<script>
export default {
  name: "Search",
  data() {
    return {
      keyword: "",
      timeout: null,
    };
  },
  methods: {
    onInput() {
      clearTimeout(this.timeout);
      this.Timeout = setTimeout(() => {
        this.search();
      }, 500);
    },
    search() {
      fetch( 
        `https://api.giphy.com/v1/gifs/search?api_key=aQ49BZok5gL8tYUtRdXG3fgRlARpU6rF&q=${this.keyword}`
      )
        .then(response => response.json())
        .then(result => {
          this.gifs = result.data;
          this.$emit("fetch-gifs", result.data);
          console.log(result);
        });
    },
  },
};
</script>

<style lang="scss" scoped>
.input-group {
  width: 100%;
  text-align: center;

  input {
    font-size: 20px;
    outline: 0;
    border: 2px solid #1345e6;
    margin-bottom: 40px;
    width: 95%;
    padding: 8px;
  }

  .btn {
    outline: 0;
    width: 5%;
    border-radius: 0;
    height: 50px;
    background: linear-gradient(
      to right,
      #1345e6 0%,
      #ed239f 51%,
      #1345e6 100%
    );
    border: none;
  }
}

@media (max-width: 767px) {
  .input-group input {
    width: 85%;
  }
  .input-group .btn {
    width: 15% !important;
  }
}
</style>
