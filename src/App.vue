<template>
  <div id="app">
    <!-- Header /-->
    <About />
    <EdCerts />
    <Skills />
    <Projects />
    <Contact />
  </div>
</template>

<script>

import About from '@/components/About';
import Contact from '@/components/Contact';
import EdCerts from "@/components/EdCerts";
//import Header from "@/components/Header";
import Projects from "@/components/Projects";
import Skills from "@/components/Skills";

export default {
  name: 'App',
  components: {
    About,
    Contact,
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
    color: #2c3e50;
    min-width: 600px;
    max-width: 1000px;
    margin: auto;
  }

  h2 {
    text-align: center;
  }

</style>
