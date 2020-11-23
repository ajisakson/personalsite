<template>
  <div id="app" :class="isDarkMode ? 'darkTheme' : 'lightTheme'" >
    <div id="main">
      <Projects />
      <Skills />
      <EdCerts />
    </div>
    <div id="sidebar">
      <About />
      <div><button @click="isDarkMode = !isDarkMode">{{ isDarkMode ? 'Light Mode' : 'Dark Mode'}}</button></div>
      <!-- Header /-->
      <!-- Contact / -->
    </div>
  </div>
</template>

<script>

import About from '@/components/About';
import EdCerts from "@/components/EdCerts";
import Projects from "@/components/Projects";
import Skills from "@/components/Skills";
//import Header from "@/components/Header";
// import Contact from '@/components/Contact';

export default {
  name: 'App',
  data() {
    return {
      isDarkMode: false,
    }
  },
  components: {
    About,
    //Contact,
    EdCerts,
    //Header,
    Projects,
    Skills
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: var(--font-color);
    background-color: var(--bg-color);
    min-width: 600px;
    max-width: 1000px;
    margin: auto;
  }
  #main {
    width: 80%;
    float: right;
  }
  #sidebar {
    width: 250px;
    float: left;
    position: fixed;
  }
  .darkTheme {
    --primary-color: #008080;
    --secondary-color: #002366;
    --font-color: #fff;
    --bg-color: #000;
  }
  .lightTheme {
    --primary-color: #fff;
    --secondary-color: #002366;
    --font-color: #000;
    --bg-color: #fff;
  }

  h2 {
    text-align: center;
  }

</style>
