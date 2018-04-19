<template>
  <ul class="skills-list row">
    <li v-for="(skill, index) in skills" :key="`skill-${index}`" class="col-sm-6">
      <h4 class="skill-title">{{ skill.title }}</h4>
      <div class="skill-progress">
        <div class="skill-percentage" :style="`width: ${skill.percent}%;`">
          <span>{{ skill.percent }}%</span>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Skills',
  props: {
    skills: {
      required: true,
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.skills-list {
  list-style-type: none;
  padding: 0;
}

.skill-title {
  display: block;
  text-transform: uppercase;
  margin-bottom: 0;
  font-size: 12px;
  font-weight: 300;
  color: #666666;
}

.skill-progress {
  background: #fff;
  border: 1px solid #14c8c8;
  border-radius: 50px;
  display: block;
  height: 16px;
  margin: 8px 0;
  overflow: hidden;
  position: relative;
  width: 100%;
}

.skill-percentage {
  background-color: #14c8c8;
  border-radius: 50px;
  bottom: 0;
  font-size: 10px;
  position: absolute;
  text-align: center;
  top: 0;

  span {
    color: #fff;
  }
}
</style>
