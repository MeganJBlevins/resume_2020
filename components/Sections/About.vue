<template>
  <section id="about">
    <div id="background-wrap">
      <!-- <div v-for="x in 10" :key="x" class="bubble" :class="'x' + x"></div> -->
    </div>
    <div class="container">
      <div class="columns">
        <div class="column about-text">
          <p class="hello">Hello, I'm</p>
          <h1>Megan Blevins</h1>
          <h2>Software/Web Developer</h2>
          <a href="mailto:meganjblevins@gmail.com"><i class="email"></i>meganjblevins@gmail.com</a>
          <a tel="4177184470"><i class="telephone"></i>417.718.4470</a>
          <span><i class="location"></i>Ozark, MO</span>
        </div>
        <div class="column">
          <div class="cartoon-headshot">
            <div class="img-border">
              <img alt="Cartoon Megan" src="@/assets/images/megan-character__headshot.png">
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'About',
}
</script>
