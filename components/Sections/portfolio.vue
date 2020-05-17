<template>
  <section id="portfolio">
    <div class="container">
    <div class="section-title">
      <h1>Portfolio</h1>
    </div>
    </div>
    <div class="container">
      <div class="columns is-multiline">
        <div class="column is-one-third" v-for="work in this.work" :key="work.index" @click="activateModal(work)" >
          <div class="card" >
            <img :src="work.image" />
            <div class="overlay">
              <h2>{{work.title}}</h2>
              <p>{{work.type}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Modal 
      v-if="this.modalActive"
      :work="this.activeWork"
      @close-modal="closeModal"
    />  
  </section>
</template>
<script>
import Modal from '~/components/UI/Modal.vue'

export default {
  name: "Portfolio",
   components: {
    Modal,
  },
  data () {
    return {
      modalActive: false,
      activeWork: {},
      work: [
        {
        "title": 'Smucker Away From Home',
        "description": "This is more about my work with Smucker Away From Home",
        "type": "Pimcore Web Development",
        "skills": ["Pimcore","Vue.js", "PHP", "Docker", "scss","html"],
        "link": "https://smuckerawayfromhome.com",
        "image": "images/SmuckersAFH.png"
        },
         {
        "title": 'Mission Food Service',
        "description": "This is more about my work with Mission Food Service",
        "type": "Umbraco/.NET MVC Web Development",
        "skills": ["Umbraco", ".NET MVC", "Microsoft SQL Server", "scss", "html"],
        "link": "http://missionfoodservice.com/",
        "image": "images/missionFoodService.png"
        },
        {
        "title": 'Mel-Fry Landing Page',
        "description": "This is more about what I did for Melfry Landing",
        "type": "Web Development",
        "skills": ["Nuxt", "Vue.js", "ScrollMagic", "Docker", "Netlify", "scss","html"],
        "link": "https://www.melfry-offer.com",
        "image": "images/melfry-offer.png"
        },
        {
        "title": 'Frame Destination',
        "description": "I have worked on many small aspects of this Magento website, including creating a module to integrate with their reviews service in order to increase site speed performance. I have also been working to migrate the site to the 2.3 Magento version. Primarily focusing on the migration of the data from one version/platform to the other.",
        "type": "Magento/Angular Web Development",
        "skills": ["Magento","Angular","PHP","html","scss"],
        "link": "https://www.framedestination.com/",
        "image": "images/FrameDestination.jpg"
        },
        {
        "title": 'Discount Party Supplies',
        "description": "I have done mostly work on migrating this website to the new 2.3 platform. I've worked to migrate the data from one version to the next, as well as creating a completely custom inventory management web application for their warehouse operation to use.",
        "type": "Magento/Laravel Web Development",
        "skills": ["Magento","Laravel","PHP","html","scss","Javascript"],
        "link": "https://www.discountPartySupplies.com/",
        "image": "images/dps.png"
        },
        {
        "title": 'Hydration Health',
        "description": "I worked to conform their previous wordpress site into the shopify CMS.",
         "type": "Shopify Ecommerce Web Development",
        "skills": ["Shopify","Liquid","html","css","Javascript"],
        "link": "https://hydrationhealth.com/",
        "image": "images/HydrationHealth.jpg"
        },
         {
        "title": "Angler's Port Marine",
        "description": "While working for Frank and Maven I was the sole developer tasked with building this highly custom Wordpress WooCommerce website. ",
         "type": "Custom Wordpress Web Development",
        "skills": ["Wordpress","PHP","html","css","Javascript"],
        "link": "https://www.anglersportmarine.com/",
        "image": "images/AnglersPortMarine.jpg"
        },
         {
        "title": 'Mother Road Motorcycles',
        "description": "This site is created using mostly a default automotive theme. The customizations come in the backend where I created multiple custom feeds for their inventory to be sent to other vendors including Cars For Sale and OVE. These were written in python and operated using an export plugin in wordpress and server cron jobs for automation.",
         "type": "Wordpress Web Development &amp; Custom Python Product Feed",
        "skills": ["Python","Wordpress","PHP","html","css","Javascript"],
        "link": "https://www.motherroadmotorcycles.com",
        "image": "images/motherRoadMotorcycles.jpg"
        },
        {
        "title": 'Clinvest Clinical Research',
        "description": "I was tasked with the complete rebuild of this website on the wordpress platform. It's a highly custom site building on the Jupiter theme.",
         "type": "Custom Wordpress Web Development",
        "skills": ["Wordpress","PHP","html","css","Javascript"],
        "link": "https://clinvest.com/",
        "image": "images/clinvest.jpg"
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