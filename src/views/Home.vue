<template>
  <div class="home">
    <!-- HomePage -->
    <div class="container">
      <search @fetch-gifs="onFetch" />
      <gif-list :gifs="gifs" />
    </div>
  </div>
</template>

<script>
import Search from "@/components/Search.vue";
import GifList from "@/components/GifList.vue";

export default {
  name: "Home",
  components: {
    Search,
    GifList,
  },
  data() {
    return {
      gifs: [],
    };
  },
  methods: {
    onFetch(result) {
      this.gifs = result;
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  margin-bottom: 50px;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    min-height: 97px;

    ul {
      list-style: none;

      router-link {
        padding: 20px 10px;
        color: #ffffff;
        text-decoration: none;
        font-size: 18px;
        transition: 0.3s;
        position: relative;
        z-index: 2;
        cursor: pointer;
        font-weight: 700;
        letter-spacing: 1px;
        font-family: Arial, Helvetica, sans-serif;

        &.active,
        &:hover {
          color: rgb(0, 102, 255);
          border-bottom: 1px solid rgb(0, 102, 255);
        }
      }
    }
  }
}
</style>
