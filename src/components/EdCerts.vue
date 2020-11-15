<template>
 <div>
   <h2>Education</h2>
   <div class="school-badge" style="display: flex; flex-wrap: wrap; justify-content: center;">
     <div v-for="school in schools" v-bind:key="school.id" style="flex: 0 1 275px;" >
       <p style="text-align: center; justify-content: center;"><i>Logo Here</i></p>
       <p>{{ school.name }}</p>
       <p>{{ school.spec }}</p>
       <p>{{ school.dates }}</p>
     </div>
   </div>
   <h2>Certifications</h2>
   <div class="cert-badge" style="display: flex; flex-wrap: wrap; justify-content: center;">
     <div  v-for="cert in certs" v-bind:key="cert.id" style="flex: 0 1 250px;">
       <p style="text-align: center; justify-content: center;"><i>Logo Here</i></p>
       <p>{{ cert.org }} {{ cert.name }}</p>
       <p>{{ cert.date }}</p>
     </div>
   </div>
 </div>
</template>

<script>

export default {
  name: "EdCerts",
  data() {
    return {
      schools: [
        {
          id: 1,
          name: 'Western Governors University',
          dates: 'September 2018 - November 2020',
          spec: 'Bachelor of Science, Software Development',
          logo: 'public/images/WGU-MarketingLogo_Natl_RGB_Owl_NoTag_4-1-2017.jpg'
        },
        {
          id: 2,
          name: 'North Idaho College',
          dates: 'August 2016 - May 2018',
          spec: 'Associate of Arts, General Studies',
          logo: 'public/images/NIClogoStacked.png'
        }
      ],
      certs: [
        {
          id: 1,
          org: 'CompTIA',
          name: 'A+',
          date: 'September 25, 2019',
          logo: 'public/images/APlusLogo.png'
        },
        {
          id: 2,
          org: 'CompTIA',
          name: 'Project+',
          date: 'April 19, 2019',
          logo: 'public/images/ProjectPlusLogo.png'
        },
        {
          id: 3,
          org: 'CIW',
          name: 'Advanced HTML5 & CSS3 Specialist',
          date: '',
          logo: 'public/images/CIWhtmlcss.jpg'
        },
        {
          id: 4,
          org: 'CIW',
          name: 'User Interface Designer',
          date: '',
          logo: 'public/images/CIWuidesign.jpg'
        }
        ,
        {
          id: 5,
          org: 'ITIL',
          name: 'Foundation v3',
          date: '',
          logo: 'public/images/itilv3.png'
        },
        {
          id: 6,
          org: 'MTA',
          name: 'HTML5 Application Developer Fundamentals',
          date: '',
          logo: 'public/images/MTAhtmlappdev.png'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>