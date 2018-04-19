<template>
  <div class="testimonials">
    <blockquote
      cite="https://www.linkedin.com/in/ederssouza/"
      v-for="(testimonial, index) in testimonials"
      :key="`testimonial-${index}`"
      class="testimonial-item"
      :class="(index % 2) ? 'even' : 'odd'">
      <div class="testimonial-avatar">
        <img :src="testimonial.avatar" :alt="testimonial.name" :title="testimonial.name">
      </div>
      <span class="testimonial-name">{{ testimonial.name }}</span>
      <span class="testimonial-occupation">{{ testimonial.occupation }}</span>
      <p class="testimonial-text">"{{ testimonial.text }}"</p>
      <small class="testimonial-connection">{{ testimonial.connection }}</small>
    </blockquote>
  </div>
</template>

<script>
export default {
  name: 'Testimonials',
  props: {
    testimonials: {
      required: true,
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
.testimonials {}

.testimonial-item {
  background-color: #f7f7f7;
  border: none;
  border-radius: 8px;
  padding: 20px;
  position: relative;

  .testimonial-avatar {
    border: 10px solid #fff;
    border-radius: 50%;
    height: 85px;
    overflow: hidden;
    position: absolute;
    top: 20px;
    width: 85px;

    img {
      left: 50%;
      max-width: 100%;
      position: absolute;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  }

  // impar
  &.odd {
    margin-right: 30px;
    padding-right: 65px;
    text-align: right;

    .testimonial-avatar {
      right: -42.5px;
    }
  }

  // par
  &.even {
    margin-left: 30px;
    padding-left: 65px;
    text-align: left;

    .testimonial-avatar {
      left: -42.5px;
    }
  }
}

.testimonial-name,
.testimonial-occupation,
.testimonial-text {
  display: block;
}

.testimonial-name {
  font-size: 15px;
  color: #444;
  margin-bottom: 2px;
  font-weight: 700;
}

.testimonial-occupation {
  font-size: 13px;
  font-weight: 400;
  margin-bottom: 5px;
}

.testimonial-text {
  color: #777;
  font-size: 80%;
  font-style: italic;
  margin-bottom: 0;
}

.testimonial-connection {
  color: #999;
  display: block;
  font-size: 60%;
  font-style: italic;
  margin-top: 10px;
}
</style>
