<template>
  <section id="skills" class="skills-wrapper">
    <pageTitle title="Skills" />
    <div class="skills">
      <ul>
        <li v-for="(skill, index) in skills" :key="index">
          {{ skill.name }}
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'
export default {
  name: 'Skills',
  components: {
    pageTitle,
  },
  data() {
    return {
      skills: [
        { name: 'HTML/CSS' },
        { name: 'Vue.js / Nuxt.js' },
        { name: 'JavaScript (ES6)' },
        { name: 'C' },
        { name: 'C++' },
        { name: 'GitHub' },
        { name: 'Python' },
        { name: 'Java' },
        { name: 'Keras' },
        { name: 'TensorFlow' },
        { name: 'PHP' },
        { name: 'cakePHP' },
      ],
    }
  },
}
</script>

<style scoped>

.skills-wrapper {
  text-align: center;
  display: flex;
  flex-wrap: wrap;
  padding: 60px 12vw;
  justify-content: center;
  &:last-child{
    border-bottom:none;
  }

  @media (max-width: 1250px) {
    padding: 30px 60px;
    border:none;
  }

  @media (max-width: 670px) {
    padding: 30px;
  }
  background-color: #ffffff;
}
.skills {
  display: flex;
  margin: 0;
  flex-wrap: wrap;

  width: 100%;
  justify-content:center;
  width: 100%;
}
ul {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  @media (max-width: 1410px) {
    grid-template-columns: repeat(2, 200px);
  }

  @media (max-width: 670px) {
    grid-template-columns: 200px;
  }
}

li {
  width: 100%;
  text-align: left;
  font-size: 16px;
  padding: 8px 0;
  color: $text-color;
}
</style>