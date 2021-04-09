<template>
    <div 
    class="portfolio-modal__container"  
    aria-modal="true"
    @click.self="closeModal"
  >
    <div class="portfolio-modal">
      <div class="close-modal">
        <button 
          type="button"
          class="modal__close"
          @click="closeModal" 
        >&times;
        </button>
      </div>
       <div class="work-image">
        <img :src="work.image" :alt="'screenshot of ' + this.work.title" />
      </div>
      <div class="work-info">
        <h2>{{ this.work.title }}</h2>
        <p>{{ this.work.description }}</p>
        <div class="skills-list">
          <p v-for="skill in this.work.skills" :key="skill.index"><span>{{ skill }}</span></p>
        </div>
        <button class="button is-primary"><a :href="this.work.link" target="_blank">View Live Site</a></button>
      </div>
     
    </div>
  </div>
</template>
<script>
export default {
  name: "Modal",
  props: {
    work: null
  },
  methods: {
    closeModal() {
      console.log('modal.vue close modal')
      this.$emit('close-modal')
    }
}

}
</script>
