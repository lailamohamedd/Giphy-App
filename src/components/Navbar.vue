<template>
  <header>
    <div class="container">
      <!-- Start Links -->
      <ul>
        <router-link to="/" tag="li">Giphy App</router-link>
        <router-link to="/signup" tag="li">sign up</router-link>
      </ul>
      <!-- End Links -->
    </div>
  </header>
</template>
<script>
export default {};
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
    
    a {
      padding: 20px 10px;
      color: #ffffff;
      font-size: 18px;
      position: relative;
      z-index: 2;
      font-family: Arial, Helvetica, sans-serif;

      &.active,
      &:hover {
        color: rgb(0, 102, 255);
        border-bottom: 1px solid rgb(0, 102, 255);
      }
    }
  }
}
</style>
