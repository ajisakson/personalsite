<template>
  <div>
    <h2>Austin Isakson</h2>
    <div style="display: flex; flex-wrap: wrap; justify-content: center;">
      <div style="flex: 1 1 200px;">
        <img id="profile-pic" :src="picture" alt="Profile Picture"/>
        <p style="text-align: center;">{{ location }}</p>
        <div id="social-links">
          <a :href="twitter"><img class="social-link" :src="require('@/assets/images/Twitter_Social_Icon_Circle_Color.png')" alt="Twitter link"/></a>
          <a :href="github"><img class="social-link" :src="require('@/assets/images/GitHub-Mark-32px.png')" alt="GitHub link"/></a>
          <a :href="linkedin"><img class="social-link" :src="require('@/assets/images/LI-In-Bug.png')" alt="LinkedIn link"/></a>
        </div>
      </div>
      <div id="bio">
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
        picture: require('@/assets/images/cheesin.jpeg'),
        location: 'Post Falls, ID',
        linkedin: 'https://linkedin.com/in/ajisakson/',
        github: 'https://github.com/ajisakson',
        twitter: 'https://twitter.com/austinisakson'
      }
    }
  }

</script>

<style scoped>

#profile-pic {
  display: block;
  margin: auto;
  width: 200px;
  border-radius: 50%;
}

#social-links {
  display: block;
}

.social-link {
  width: 32px;
  margin: 4px;
}

#bio {
  flex: 0 1 250px;
}

</style>