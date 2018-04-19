<template>
  <header class="profile-avatar">
    <img :src="image" :alt="title" :title="title">
  </header>
</template>

<script>
export default {
  props: {
    image: {
      required: true,
      type: String
    },
    title: {
      required: true,
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
.profile-avatar {
  position: relative;

  &:before {
    background: -moz-linear-gradient(left, rgba(51,55,61,1) 0%, rgba(51,55,61,0) 100%);
    background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(51,55,61,1)), color-stop(100%,rgba(51,55,61,0)));
    background: -webkit-linear-gradient(left, rgba(51,55,61,1) 0%,rgba(51,55,61,0) 100%);
    background: -o-linear-gradient(left, rgba(51,55,61,1) 0%,rgba(51,55,61,0) 100%);
    background: -ms-linear-gradient(left, rgba(51,55,61,1) 0%,rgba(51,55,61,0) 100%);
    background: linear-gradient(to left, rgba(51,55,61,1) 0%,rgba(51,55,61,0) 100%);
    color: #ffffff;
    content: "Eder Sampaio \00ae";
    display: block;
    font-size: 10px;
    line-height: 15px;
    left: -20.5%;
    opacity: .95;
    padding: 2px 15px 2px 30px;
    position: absolute;
    text-transform: uppercase;
    top: 20.5%;
    z-index: 1;
    -webkit-transform: rotate(-90deg);
    -ms-transform: rotate(-90deg);
    transform: rotate(-90deg);
  }

  img {
    max-width: 100%;
  }
}
</style>
