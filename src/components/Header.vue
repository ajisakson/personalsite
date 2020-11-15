<template>
  <div class="header">
    <h3>About</h3>
    <h3>School</h3>
    <h3>Certs</h3>
    <h3>Skills</h3>
    <h3>Projects</h3>
    <h3>Contact</h3>
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
h3 {
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
h3:hover {
  background: #2c3e50;
  color: #fff;
}
</style>