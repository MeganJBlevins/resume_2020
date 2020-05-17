<template>
  <section id="about">
    <div class="gradient-container">
    <!-- <div id="background-wrap"> -->
      <!-- <div v-for="x in 10" :key="x" class="bubble" :class="'x' + x"></div> -->
    <!-- </div> -->
      <div class="container gradient">
        <div class="columns">
          <div class="column about-text">
            <p class="hello">Hello, I'm</p>
            <h1>Megan Blevins</h1>
            <h2>Software/Web Developer</h2>
            <a href="mailto:meganjblevins@gmail.com">
              <Email />
              meganjblevins@gmail.com
            </a>
            <a tel="4177184470">
              <Telephone />
              417.718.4470
            </a>
            <span>
              <Location />
              Ozark, MO
            </span>
          </div>
          <div class="column">
            <div class="cartoon-headshot">
              <div class="img-border">
                <img alt="Cartoon Megan" src="images/megan-character__headshot.png">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="columns coffee-text">
        <div class="column coffee-image">
          <img src="images/first-coffee.jpg" alt="but first, coffee"/>
        </div>
        <div class="column">
          <h2 class="h1">About Me</h2>
          <p>Hello, I’m a Megan, web developer based in Ozark, Missouri. 
            I have a rich history in development, and work with many different platforms, frameworks, 
            languages and environments! Working in a couple different agency-style positions has made 
            my ability to assess and adapt to new projects and environments easily! I'm looking for a long-term 
            development home. I'm looking to find a place that I can grow and learn and develop my skills as 
            I'm always looking for a new project to expand my knowledge pool! Do you think I would fit with your company? 
            I'd love to find out!</p>
            <button class="button is-primary"><a href="#">Download Resume <Download /></a></button>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import Email from '~/components/Icons/Email.vue'
import Telephone from '~/components/Icons/Telephone.vue'
import Location from '~/components/Icons/Location.vue'
import Download from '~/components/Icons/Download.vue'

export default {
  name: 'About',
  components: {
    Email,
    Telephone,
    Location,
    Download
  }
}
</script>
