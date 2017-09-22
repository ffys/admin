<template>
  <router-view></router-view>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
/*  // Import Font Awesome Icons Set*/
  $fa-font-path: "~font-awesome/fonts/";
  @import "~font-awesome/css/font-awesome.min.css";
/* Import Simple Line Icons Set*/
  $simple-line-font-path: "~simple-line-icons/fonts/";
  @import "~simple-line-icons/css/simple-line-icons.css";
</style>
<style lang="scss">
  // Import Main styles for this application
  @import "./scss/style";
  body {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    font-family: Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
  }
</style>

