<template>
  <div class="row">
    <!-- Start Gif List -->
    <div id="gifList">
      <gif v-for="gif in gifs" :key="gif.id" :gif="gif" />
    </div>
    <!-- End Gif List -->
  </div>
</template>

<script>
// Import components
import Gif from "@/components/Gif";

export default {
  name: "GifList",
  components: { Gif },
  props: {
    gifs: Array,
  },
}
</script>

<style scoped>
#gifList {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
