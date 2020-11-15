<template>
  <div>
    <h2>Some Stuff I Made</h2>
    <div class="portfolio">
      <div class="project" v-for="project in projects" v-bind:key="project.id">
        <p style="justify-content: center; text-align: center;"><i>Preview Here</i></p>
        <p style="text-align: center;">{{ project.title }}</p>
        <p>{{ project.description }}</p>
        <p>{{ project.link }}</p>
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
          preview: ''
        },
        {
          id: 2,
          title: 'WGUTermScheduler',
          description: 'An Android app for scheduling terms, classes, and adding notes for school using Android API 29, Java, and Gradle for package management. Developed using Android Studio and a standard local SQLite database implementation.',
          link: 'https://github.com/ajisakson/WGUScheduler',
          preview: ''
        },
        {
          id: 3,
          title: 'GuildMasterBot',
          description: '',
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
}

.project{
  flex: 0 1 300px;
  margin: 0 20px 0 20px;
}

</style>