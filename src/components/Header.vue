<template>
  <div class="header">
    <h2>About</h2>
    <h2>School</h2>
    <h2>Certs</h2>
    <h2>Skills</h2>
    <h2>Projects</h2>
    <h2>Contact</h2>
  </div>
</template>

<script>
export default {
name: "Header"
}
</script>

<style scoped>
.header {
  float: left;
  width: 120px;
  margin-left: 25%;
  text-align: right;
  position: static;
}
h2{
  padding-top: 7px;
  padding-bottom: 5px;
  padding-right: 10px;
  display: block;
  background: darkcyan;
  color: #fff;
  height: 35px;
  margin-bottom: 0;
  margin-top: 0;
}
h2:hover{
  background: #2c3e50;
  color: #fff;
}
</style>