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

        <div id="nerd-achievements">
          <h4>Nerd Achievements:</h4>
          <p><i>Insert claim to fame here via JS</i></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "About",
    data() {
      return {
        bio: "Hey! Thanks for checking out my virtual résumé! I'm currently looking for a local or remote position where I can continue to develop my skills as a software engineer and gain experience while contributing to the organization's needs. I'm happy to learn new technologies and work in a team environment.",
        claimstofame: ['Top 50 warlock on biggest realm in WoW','Top 0.5% of players in Teamfight Tactics','Only had to rewatch Arrested Development twice to get all of the jokes','Primary target of impostor kills in Among Us','Captain of high school Varsity Quiz Bowl team','Voluntarily quarantined for years before Covid'],
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
  font-size: .9em;
}

</style>