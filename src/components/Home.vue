<template>
  <div class="home">
    <div class="container">
      <div class="row">
        <div class="col-md-3">
          <cv-profile />
        </div><!-- /.col -->

        <div class="col-md-9">
          <cv-content />
        </div><!-- /.col -->
      </div><!-- /.row -->
    </div><!-- /.container -->
  </div>
</template>

<script>
import Profile from './Profile'
import Content from './Content'

export default {
  name: 'Home',
  components: {
    'cv-profile': Profile,
    'cv-content': Content
  }
}
</script>

<style lang="scss" scoped>
</style>
