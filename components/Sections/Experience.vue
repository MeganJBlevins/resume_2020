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
    <div class="container">
    <div class="section-title">
      <h1>Education</h1>
    </div>
    </div>
    <div class="container experience-list">
      <div class="card" v-for="school in this.education" :key="school.dates">
        <h2>{{school.degree}} <span>{{school.school}}</span></h2>
        <p class="dates">{{school.dates}}</p>
        <p class="description">{{school.description}}</p>
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
          "description": "lorem ipsum"
        }, {
          "title": "Software/Web Developer",
          "company": "Web Arc Technologies",
          "dates" : "September 2018 - August 2019",
          "description": "Working with WebArc Technologies I create and maintain highly custom websites on both the Wordpress and Magento platforms. The most recent and by far the most exciting project I’ve worked on is creating a completely custom multi-warehouse inventory management system using the Laravel framework from the ground up. Other items I've created are custom modules for the Magento platform, as well as migrating 1.x sites to the new 2.3 version. Additionally, I have also created intricate Wordpress sites utilizing Custom Post Types that form relationships using Advanced Custom Fields."
        }, {
          "title": "Lead Web Developer",
          "company": "Frank and Maven",
          "dates": "July, 2017 - September 2018",
          "description": "As the sole developer for Frank and Maven, I managed nearly 100 unique web servers and nearly 130 different websites. Most of these were on the Wordpress platform, while others were on Magento, Shopify and even completley custom frameworks. My role was not only one to complete the technical aspects of the job, but also to help advise and communicate with clients on their technical/web needs."
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
          "dates": "May, 2008",
          "description": "I went to school for broadcasting focusing on videography and video editing. I went into broadcasting as a director and later producer at a local television station, but decided that the work schedule of a news station just wasn't going to be for me long-term. I decided to find something that was more flexible and conducive to my future family plans."
        }
      ]
    }
  }
}
</script>