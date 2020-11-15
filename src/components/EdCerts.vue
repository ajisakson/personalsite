<template>
 <div>
   <h2>Education</h2>
   <div class="school-list">
     <div class="school-badge" v-for="school in schools" v-bind:key="school.id">
       <img :src="school.logo" alt="School Logo"/>
       <p>{{ school.name }}</p>
       <p>{{ school.spec }}</p>
       <p>{{ school.dates }}</p>
     </div>
   </div>
   <h2>Certifications</h2>
   <div class="cert-list">
     <div class="cert-badge" v-for="cert in certs" v-bind:key="cert.id">
       <img :src="cert.logo" alt="Certification Logo"/>
       <p>{{ cert.org }} {{ cert.name }}
       <br/>{{ cert.date }}</p>
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
          logo: require('@/assets/images/WGU-MarketingLogo_Natl_RGB_Owl_NoTag_4-1-2017.jpg')
        },
        {
          id: 2,
          name: 'North Idaho College',
          dates: 'August 2016 - May 2018',
          spec: 'Associate of Arts, General Studies',
          logo: require('@/assets/images/NIClogoStacked.png')
        }
      ],
      certs: [
        {
          id: 1,
          org: 'CompTIA',
          name: 'A+',
          date: 'September 25, 2019',
          logo: require('@/assets/images/APlusLogo.png')
        },
        {
          id: 2,
          org: 'CompTIA',
          name: 'Project+',
          date: 'April 19, 2019',
          logo: require('@/assets/images/ProjectPlusLogo.png')
        },
        {
          id: 3,
          org: 'CIW',
          name: 'Advanced HTML5 & CSS3 Specialist',
          date: '',
          logo: require('@/assets/images/CIWhtmlcss.jpg')
        },
        {
          id: 4,
          org: 'CIW',
          name: 'User Interface Designer',
          date: '',
          logo: require('@/assets/images/CIWuidesign.jpg')
        }
        ,
        {
          id: 5,
          org: 'ITIL',
          name: 'Foundation v3',
          date: '',
          logo: require('@/assets/images/itilv3.png')
        },
        {
          id: 6,
          org: 'MTA',
          name: 'HTML5 Application Developer Fundamentals',
          date: '',
          logo: require('@/assets/images/MTAhtmlappdev.png')
        }
      ]
    }
  }
}
</script>

<style scoped>
  .school-list {
    display: flex; flex-wrap: wrap; justify-content: center;
  }
  .school-badge {
    flex: 0 1 275px;
    margin: 20px;
  }
  .school-badge img {
    width: 275px;
  }
  .cert-list {
    display: flex; flex-wrap: wrap; justify-content: center;
  }
  .cert-badge {
    flex: 0 1 250px;
    text-align: center;
  }
  .cert-badge img {
    height: 150px;
  }

</style>