<template>
  <div>
    <h2>Skills</h2>
    <div class="skills-list">
      <div class="skill-item" v-for="item in set" v-bind:key="item">
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills",
    data() {
      return {
        set: ['Java', 'JavaFX MVC', 'MySQL', 'Git', 'HTML', 'CSS', 'JavaScript', 'Gradle', 'Maven', 'Android', 'Linux (Debian)', 'Vue.js', 'C++', 'Python', 'Django', 'Agile', 'Scrum']
      }
    }
}
</script>

<style scoped>
  .skills-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 70%;
    margin: auto;
  }
  .skill-item {
    background: var(--primary-color);
    color: var(--font-color);
    margin: 7px;
    padding: 8px 10px 8px 10px;
    font-weight: bold;
    text-transform: uppercase;
  }

</style>