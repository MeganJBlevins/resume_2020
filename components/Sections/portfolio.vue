<template>
  <section id="portfolio">
    <div class="container">
    <div class="section-title">
      <h1>Portfolio</h1>
      <p class="mobile-description">Click to Learn More</p>
    </div>
    </div>
    <div class="container">
      <div class="columns is-multiline">
        <div class="column is-one-third" v-for="work in this.work" :key="work.index" @click="activateModal(work)" >
          <div class="card" >
            <img :src="work.image" />
              <div class="overlay">
                <Click />
                <h2>{{work.title}}</h2>
                <p>{{work.type}}</p>
              </div>
          </div>
        </div>
      </div>
    </div>
    <transition 
      name="fade"
      @after-enter="modalActive = true"
    >
      <Modal 
        v-if="this.modalActive"
        :work="this.activeWork"
        @close-modal="closeModal"
      />  
    </transition>
  </section>
</template>
<script>
import Modal from '~/components/UI/Modal.vue'
import Click from '~/components/Icons/Click.vue'

export default {
  name: "Portfolio",
   components: {
    Modal,
    Click
  },
  data () {
    return {
      modalActive: false,
      activeWork: {},
      work: [
        {
        "title": 'Smucker Away From Home',
        "description": "This project is built on the Pimcore platform using PHP. It includes multiple campaign SPAs, a custom product filter app, and a custom product import.",
        "type": "Pimcore Web Development",
        "skills": ["Pimcore","Vue", "PHP", "Docker", "scss","HTML"],
        "link": "https://smuckerawayfromhome.com",
        "image": "images/Smuckerawayfromhome.jpg"
        },
         {
        "title": 'Mission Food Service',
        "description": "Mission Food Service is based on the Umbraco platform with a custom built Recipe database API integration.",
        "type": "Umbraco Web Development",
        "skills": ["Umbraco", ".NET", "Microsoft SQL Server", "scss", "HTML"],
        "link": "http://missionfoodservice.com/",
        "image": "images/missionFoodService.png"
        },
        {
        "title": 'Mel-Fry Landing Page',
        "description": "I was involved in this project from start to finish. The desktop version utilizes scroll magic to control the entering and exiting of the uncooked and cooked versions of the dishes.",
        "type": "Nuxt/Vue Web Development",
        "skills": ["Nuxt", "Vue", "ScrollMagic", "Netlify", "scss","HTML", "Netlify"],
        "link": "https://www.melfry-offer.com",
        "image": "images/melfry-landing.png"
        },
        {
        "title": "Summit Hill Foods Professional Solutions",
        "description": "This is a custom Wordpress development. Heavily utilizing ACF fields and custom templating. I created the recipes and blog filter app in vue and continue to manage updates as this site merges with the JMS Premium foods brand.",
         "type": "Custom Wordpress Web Development",
        "skills": ["Wordpress","PHP","HTML","scss","Vue"],
        "link": "https://www.anglersportmarine.com/",
        "image": "images/shfoodspro.jpg"
        },
        {
        "title": 'Rethink How You Butter',
        "description": "This is a simple Nuxt landing page hosted on Netlify connected to an AirTable API to collect leads for the SunGlow brand.",
         "type": "Custom Wordpress Web Development",
        "skills": ["Nuxt", "Vue", "HTML", "AirTable", "Netlify"],
        "link": "https://rethinkhowyoubutter.com/",
        "image": "images/rethinkhowyoubutter.jpg"
        },
        {
        "title": 'Frame Destination',
        "description": "Working on many smaller aspects of this site, I worked to maintain and provide feature upgrades, including creating a module to integrate with their reviews service in order to increase site speed performance. I was also tasked with supporting the migration of the data of this site to the 2.3 version.",
        "type": "Magento/Angular Web Development",
        "skills": ["Magento","Angular","PHP","html","scss"],
        "link": "https://www.framedestination.com/",
        "image": "images/FrameDestination.jpg"
        },
        {
        "title": 'Discount Party Supplies',
        "description": "Most of the work I did for DPS was to migrate their database from the 1.x Magento version to 2.3 version. Additionally, utilizing the Laravel framework, I created a Warehouse Management system that integrated with Magento to support the business."
        "type": "Magento/Laravel Web Development",
        "skills": ["Magento","Laravel","PHP","html","scss","Javascript"],
        "link": "https://www.discountPartySupplies.com/",
        "image": "images/dps.png"
        },
        {
        "title": 'Hydration Health',
        "description": "Hydration Health had an existing Wordpress site that linked to their Shopify shop via a subdomain. In order to streamline the purchase process, we pulled their site into Shopify and eliminating the need for the Wordrpess integration.",
         "type": "Shopify Ecommerce Web Development",
        "skills": ["Shopify","Liquid","html","css","Javascript"],
        "link": "https://hydrationhealth.com/",
        "image": "images/HydrationHealth.jpg"
        },
         
         {
        "title": 'Mother Road Motorcycles',
        "description": "This site is created using mostly a default automotive theme. The customizations come in the backend where I created multiple custom feeds for their inventory to be sent to other vendors including Cars For Sale and OVE. These were written in python and operated using an export plugin in wordpress and server cron jobs for automation.",
         "type": "Wordpress & Custom Python Product Feed",
        "skills": ["Python","Wordpress","PHP","html","css","Javascript"],
        "link": "https://www.motherroadmotorcycles.com",
        "image": "images/motherRoadMotorcycles.jpg"
        },
        
      ]
    }

  },
  methods: {
    activateModal(work) {
      this.modalActive = true
      this.activeWork = work
    },
    closeModal(){
      console.log('portfolio.vue close modal')
      this.modalActive = false
      this.activeWork = {}
    }
  }
}
</script>