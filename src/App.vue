<template>
  <div id="pp">
    <!-- Loader -->
    <pageLoader />
    <!-- Start Header -->
    <Navbar />
    <router-view></router-view>
  </div>
</template>

<script>
import pageLoader from "@/components/pageLoader.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  name: "App",
  components: {
    pageLoader,
    Navbar
  },
};
</script>
