<template>
  <ul class="courses row">
    <li v-for="(course, index) in courses" :key="`course-${index}`" class="col-sm-6">
      <img :src="course.img" :alt="course.institution" :title="course.institution">
      <div class="course-info">
        <span class="course-title">{{ course.name }}</span>
        <span class="course-subtitle" v-if="course.institution">{{ course.institution }} | <i class="ion-calendar"></i> {{ course.workload }}</span>
        <!-- <span class="course-period"><i class="ion-calendar"></i> {{ course.workload }}</span> -->
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Courses',
  props: {
    courses: {
      required: true,
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.courses {
  list-style-type: none;
  padding: 0;

  li {
    margin-bottom: 30px;

    &:before,
    &:after {
      clear: both;
      content: "";
      display: block;
    }

    img {
      float: left;
      margin-right: 15px;
      width: 45px;
    }

    .course-info {
      overflow: hidden;
    }
  }
}

.course-title,
.course-subtitle,
.course-period {
  display: block;
}

.course-title {
  font-size: 15px;
  color: #444;
  margin-bottom: 2px;
  font-weight: 700;
}

.course-subtitle {
  font-size: 13px;
  font-weight: 400;
  margin-bottom: 5px;
}

.course-period {
  font-size: 80%;
  font-style: italic;
  margin-bottom: 10px;

  i {
    margin-right: 3px;
  }
}
</style>
