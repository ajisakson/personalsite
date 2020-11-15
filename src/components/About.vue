<template>
  <div>
    <h2>About Me</h2>
    <div style="display: flex; flex-wrap: wrap; justify-content: center;">
      <div style="flex: 0 1 200px;">
        <p style="text-align: center; justify-content: center;"><i>Picture Here!</i></p>
        <p>{{ location }}</p>
        <p>{{ github }}</p>
      </div>
      <div style="flex: 0 1 400px;">
        <p>{{ bio }}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "About",
    data() {
      return {
        bio: "My name is Austin. I'm a recently graduated software engineer looking for an entry level position where I can learn and solidify my engineering disciplines while contributing to the organization.",
        picture: '',
        location: 'Post Falls, ID',
        github: 'github.com/ajisakson'
      }
    }
  }

</script>

<style scoped>

</style>