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
          "description": "Working with a great team at Marlin Network has helped me increase my skills exponentially in both front-end and back-end development as well as dev-ops. Most of our sites are running on Umbraco, a C# CMS Platform. However, the majority of my time was spent working with Smucker Away From Home on a Pimcore-based website written in PHP. This site (and many other sites we worked on) include several vue apps and also includes a headless Magento integration for ecommerce that was almost exclusively worked on by me. Another notable project (that you can see below) is the MelFry landing page done for Ventura Foods. It was a very complex scroll-based design written in Nuxt/Vue.js using Scroll Magic. We also are in the process of moving all of our sites from local servers to a cloud-based server environment on Azure."
        }, {
          "title": "Software/Web Developer",
          "company": "Web Arc Technologies",
          "dates" : "September 2018 - August 2019",
          "description": "Working with WebArc Technologies I created and maintained highly custom websites on both the Wordpress and Magento platforms. The most notable project I worked on was to create a completely custom multi-warehouse inventory management system using the Laravel framework. Other projects I worked on are custom modules for the Magento platform, as well as migrating Magento 1.x sites to the new 2.3 version. Additionally, I created advanced Wordpress sites following intricate designs. These sites included image mapping, gated content, and countless custom variables to create beautiful dynamic websites."
        }, {
          "title": "Lead Web Developer",
          "company": "Frank and Maven",
          "dates": "July, 2017 - September 2018",
          "description": "As the lead developer for Frank and Maven, I managed nearly 100 unique web servers and nearly 130 different websites. Most of these were on the Wordpress platform, while others were on Magento, Shopify and even completley custom frameworks. My role was not only one to complete the technical aspects of the job, but also to help advise and communicate with clients on their technical/web needs."
        }, {
          "title": "Freelance Web Developer",
          "company": "Shiny Metal Marketing",
          "dates": "March, 2016 - July 2017",
          "description": "Working freelance as a web developer and designer I created mostly static bootstrap websites with a few more intricate e-commerce WooCommerce/Wordpress sites thrown in. You can see more of my portfolio below."
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