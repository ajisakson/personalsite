<template>
  <div>
    <h2>Projects</h2>

    <div class="portfolio">
      <p style="width: 80%"><i>Disclaimer: I'm neither a performance artist nor a video editor so please excuse my sloppiness on the previews.</i></p>
      <div class="project" v-for="project in projects" v-bind:key="project.id">
        <video muted controls style="width: 300px;">
          <source :src="project.preview"
                  type="video/webm">
        </video>
        <p>{{ project.description }}</p>
        <button>
          <a :href="project.link">
            <img :src="require('@/assets/images/GitHub-Mark-32px.png')" alt="Github Logo"/>
            <div class="vl"></div><div class="project-title">{{ project.title }}</div>
          </a>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: "Projects",
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'ConsultCal',
          description: 'Senior Capstone project written using JDK 11, OpenJFX, package handling with Maven, and communicating with a MySQL server via JDBC. The application allows secure login, appointment and client creation, read, update, and delete functionality, input validation and error handling, as well as the ability to export appointments and clients to CSV.',
          link: 'https://github.com/ajisakson/ConsultCalMaven',
          preview: require('@/assets/video/ConsultCalEx.webm')
        },
        {
          id: 2,
          title: 'WGUTermScheduler',
          description: 'An Android app for scheduling terms, classes, and adding notes for school using Android API 29, Java, and Gradle for package management. Developed using Android Studio and a standard local SQLite database implementation.',
          link: 'https://github.com/ajisakson/WGUScheduler',
          preview: require('@/assets/video/WGUSchedulerEx.webm')
        },
        {
          id: 3,
          title: 'GuildMasterBot',
          description: 'Currently in the planning phase, Vue.js, DynamoDB, Express.js, Python, event planner for WoW guilds and other Discord communities to plan events and notify members of their Discord server.',
          link: '',
          preview: ''
        },
      ]
    }
  }
}
</script>

<style scoped>
.portfolio {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-left: 20px;
}

.project{
  flex: 0 1 300px;
  background-color: var(--primary-color);
  padding: 20px;
  margin: 10px;
}

button {
  height: 24px;
  box-shadow: 1px 1px #bbb;
}
button a {
  text-decoration: none;
  font-weight: bold;
  color: black;
}

button img {
  float: left;
  height: 16px;
}

.vl {
  border-left: 1px solid #aaa;
  height: 18px;
  float: left;
  margin: 0 6px 2px;
}

.project-title {
  margin-top: 1px;
  margin-bottom: 0;
  float: right;
}
</style>