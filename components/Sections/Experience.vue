<template>
  <section id="experience">
    <div class="container">
    <div class="section-title">
      <h1>Work Experience</h1>
    </div>
    </div>
    <div class="container experience-list">
      <div class="card" v-for="job in this.experience" :key="job.dates">
        <h2>{{job.title}} <span>{{job.company}}</span></h2>
        <p class="dates">{{job.dates}}</p>
        <p class="description">{{job.description}}</p>
      </div>
    </div>
    <div class="container education">
    <div class="section-title">
      <h1>Education</h1>
    </div>
    </div>
    <div class="container experience-list">
      <div class="card" v-for="school in this.education" :key="school.dates">
        <h2>{{school.degree}} <span>{{school.school}}</span></h2>
        <p class="dates">{{school.dates}}</p>
        <p v-if="school.description" class="description">{{school.description}}</p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Experience",
  data () {
    return {
      experience: [
        { "title": "Web Developer",
          "company": "Advantage Solutions (Marlin Network)",
          "dates" : "August, 2019 - Present",
          "description": "While working with the fantastic team at Marlin Network, I have had the opportunity to work with many technologies and languages I wasn't previously familiar with.  The project I spent the most time with at Marlin Network has been Smucker Away From Home on a Pimcore-based website written in PHP. This site (and many other sites we worked on) include several vue apps as well as a headless Magento integration for ecommerce. You can see that website in my portfolio below. Another notable project (also below) is the MelFry landing page done for Ventura Foods. It was a very complex scroll-based design written in Nuxt/Vue.js using Scroll Magic. Most of our sites run on Umbraco, a .Net based platform written in C#, and so we also worked to migrate our servers to Azure to implement a smoother development process."
        }, {
          "title": "Software/Web Developer",
          "company": "Web Arc Technologies",
          "dates" : "September 2018 - August 2019",
          "description": "Working with WebArc Technologies I created and maintained highly custom websites on both the Wordpress and Magento platforms. The most notable project I worked on was to create a completely custom multi-warehouse inventory management system using the Laravel framework. Other projects I worked on are custom modules for the Magento platform, as well as migrating Magento 1.x sites to the new 2.3 version. Additionally, I created advanced Wordpress sites following intricate designs. These sites included image mapping, gated content, and countless custom variables to create beautiful dynamic websites."
        }, {
          "title": "Lead Web Developer",
          "company": "Frank and Maven",
          "dates": "July, 2017 - September 2018",
          "description": "As the lead developer for Frank and Maven, I managed nearly 100 unique web servers and nearly 130 different websites. Most of these were on the Wordpress platform, while others were on Magento, Shopify and even completely custom frameworks. My role was not only one to complete the technical aspects of the job, but also to help advise and communicate with clients on their technical/web needs."
        }
      ],
      education: [
        {
          "degree": "B.S. in Broadcast Media",
          "school": "University of Central Missouri",
          "dates": "May, 2008"
        }
      ]
    }
  }
}
</script>