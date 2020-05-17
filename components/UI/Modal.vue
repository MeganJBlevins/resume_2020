<template>
  <div 
    class="portfolio-modal__container"  
    aria-modal="true"
    @click.self="closeModal"
  >
    <div class="portfolio-modal columns">
      <div class="close-modal">
        <button 
          type="button"
          class="modal__close"
          @click="closeModal" 
        >&times;
        </button>
      </div>
      <div class="column work-info">
        <h2>{{ this.work.title }}</h2>
        <p>{{ this.work.description }}</p>
        <ul>
          <li v-for="skill in this.work.skills" :key="skill.index">{{ skill }}</li>
        </ul>
        <button class="button is-primary"><a :href="this.work.link">View Live Site</a></button>
      </div>
      <div class="column work-image">
        <img :src="'../../assets/images/' + this.work.image" :alt="'screenshot of ' + this.work.title" />
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
