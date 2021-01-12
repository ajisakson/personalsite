<template>
  <div>
    <h2>Austin Isakson</h2>
    <div id="profile-pic">
      <img :src="picture" alt="Profile Picture"/>
    </div>
    <div id="location">
      <p style="display: block; width: 100%; padding-left: 15px;">{{ location }}</p>
    </div>
    <div id="social-links">
      <a :href="twitter"><img class="social-link" :src="require('@/assets/images/Twitter_Social_Icon_Circle_Color.png')" alt="Twitter link"/></a>
      <a :href="github"><img class="social-link" :src="require('@/assets/images/GitHub-Mark-32px.png')" alt="GitHub link"/></a>
      <a :href="linkedin"><img class="social-link" :src="require('@/assets/images/LI-In-Bug.png')" alt="LinkedIn link"/></a>
    </div>
    <div id="bio">
      <p>{{ bio }}</p>
    </div>
    <div id="nerd-achievements">
      <h4>Nerd Achievements:</h4>
      <p><i>Insert claim to fame here via JS</i></p>
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
  margin: 0 auto 10px auto;
  width: 200px;
}

#profile-pic img {
  width: 200px;
  border-radius: 50%;
}

#location {
  display: block;
  margin: auto;
  padding: 1px 10px 1px 10px;
  width: 300px;
  background-color: var(--primary-color);
}

#social-links {
  display: block;
  margin: auto;
  padding: 0 0 0 20px;
  width: 300px;
  background-color: var(--primary-color);
}

.social-link {
  display: inline-block;
  width: 32px;
  margin: 0 5px 0 5px;

}

#bio {
  display: block;
  background-color: var(--primary-color);
  padding: 10px 10px 5px 10px;
  margin: auto;
  width: 300px;
}

#nerd-achievements {
  display: none;
  background-color: var(--primary-color);
}
</style>