<template>
  <!-- Start Search Form -->
  <div class="gif" :style="`background-image: url(${gif.images.original.url}) `">
    <input ref="url" readonly type="text" :value="gif.images.original.url" style="flex: l"/>
    <i @click="copyUrl" class="fa fa-link"></i>
  </div>
  <!-- End Search Form -->
</template>
<script>

export default {
  name: "Gif",
  props: {
    gif: Object,
  },
  methods: {
    copyUrl() {
      this.$refs.url.select();
      document.execCommand("copy");
      this.$refs.url.value = "copied!!!";
    },
  },
}
</script>

<style lang="scss" scoped>

.gif {
  width: 260px;
  max-width: 100%;
  height: 250px;
  background-repeat: no-repeat;
  background-position: center;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin-bottom: 30px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  border-radius: 5px;

  .fa {
    color: #fff;
    padding: 10px;
    font-size: 20px;
    cursor: pointer;
  }
  input {
    margin: 10px;
    background: transparent;
    color: #fff;
  }
}

@media (max-width: 767px) {
  .gif {
    width: 100%;
  }
}
</style>
