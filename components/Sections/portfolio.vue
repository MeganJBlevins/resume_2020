<template>
  <section id="portfolio">
    <div class="container">
    <div class="section-title">
      <h1>Portfolio</h1>
    </div>
    </div>
    <div class="container">
      <div class="columns">
        <div class="column" >
          <div class="card" v-for="work in this.work" :key="work.index">
            <h2>{{work.title}} </h2>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Portfolio",
  data () {
    return {
      work: [
        {
        "title": 'this is a work item'
        }
      ]
    }
  }
}
</script>