<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
// Core variables and mixins
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/variables";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/mixins";

// Reset and dependencies
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/normalize";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/print";

// Core CSS
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/scaffolding";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/type";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/code";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/grid";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/forms";

// Utility classes
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/utilities";
@import "../node_modules/bootstrap-sass/assets/stylesheets/bootstrap/responsive-utilities";

body {
  background-color: #efefef;
  color: #999;
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  padding: 50px 0;
}
</style>
