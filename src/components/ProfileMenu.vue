<template>
  <ul class="profile-menu">
    <li v-for="(link, index) in links" :key="index">
      <a href="#" :title="link.title" :class="link.active ? 'active' : ''"><i :class="link.icon"></i> {{ link.title }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ProfileMenu',
  props: {
    links: {
      required: true,
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.profile-menu {
  list-style-type: none;
  margin-bottom: 0;
  padding-left: 0;

  li {
    position: relative;
    border-bottom: 1px solid #26292e;

    &:last-child {
      border-bottom: none;
    }

    > a {
      background-color: #33373d;
      color: #85878b;
      display: block;
      font-size: 12px;
      font-weight: 500;
      padding: 15px 25px;
      text-align: right;
      text-transform: uppercase;
      -webkit-transform: translateZ(0);
      -ms-transform: translateZ(0);
      transform: translateZ(0);
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      -ms-transition-property: color;
      -webkit-transition-property: color;
      transition-property: color;
      -webkit-transition-duration: 0.3s;
      transition-duration: 0.3s;
      width: 100%;

      i {
        font-size: 24px;
        left: 25px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
      }

      &:before {
        background-color: #14c8c8;
        bottom: 0;
        content: "";
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        z-index: -1;
        -webkit-transform: scaleX(0);
        -ms-transform: scaleX(0);
        transform: scaleX(0);
        -webkit-transform-origin: 50%;
        -ms-transform-origin: 50%;
        transform-origin: 50%;
        -webkit-transition-property: transform;
        -ms-transition-property: transform;
        transition-property: transform;
        -webkit-transition-duration: 0.3s;
        -ms-transition-duration: 0.3s;
        transition-duration: 0.3s;
        -webkit-transition-timing-function: ease-out;
        -ms-transition-timing-function: ease-out;
        transition-timing-function: ease-out;
      }

      &:focus,
      &:hover,
      &.active {
        color: #fff;
        text-decoration: none;

        &:before {
          -webkit-transform: scaleX(1);
          -ms-transform: scaleX(1);
          transform: scaleX(1);
        }
      }
    }
  }
}
</style>
