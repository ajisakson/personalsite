<template>
  <div id="app" :class="isDarkMode ? 'darkTheme' : 'lightTheme'" >
    <div class="container;">
      <div id="main" class="not-mobile">
        <Projects />
        <Skills />
        <EdCerts />
      </div>
      <div id="sidebar" class="not-mobile">
        <div><button class="theme_switch_btn" @click="isDarkMode = !isDarkMode">{{ isDarkMode ? 'Light Mode' : 'Dark Mode'}}</button></div>
        <About />
        <!-- Header /-->
        <!-- Contact / -->
      </div>
    </div>
    <div class="container; mobile">
      <About />
      <div><button class="theme_switch_btn" @click="isDarkMode = !isDarkMode">{{ isDarkMode ? 'Light Mode' : 'Dark Mode'}}</button></div>
      <Skills />
      <EdCerts />
      <Projects />
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
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow: auto;
  }
  .container {
    margin: auto;
    min-width: 600px;
    max-width: 1000px;
  }
  #main {
    width: 70%;
    float: right;
    background-color: var(--secondary-color);
    padding-left: 80px;
  }
  #sidebar {
    width: 30%;
    height: 100%;
    float: left;
    padding-left: 40px;
    position: fixed;
    background-color: var(--secondary-color);
  }
  .darkTheme {
    --primary-color: #004040;
    --secondary-color: #000b1a;
    --font-color: #ffffff;
    --bg-color: #100f0f;
  }
  .lightTheme {
    --primary-color: #fff;
    --secondary-color: #fff;
    --font-color: #000;
    --bg-color: #fff;
  }

  .theme_switch_btn {
    display: block;
    margin: 20px auto auto;
  }

  h2 {
    text-align: center;
  }

  @media screen and (min-width: 950px){
    .mobile {
      display: none;
    }
  }

  @media screen and (max-width: 949px){
    .not-mobile {
      display: none;
    }
  }



</style>
