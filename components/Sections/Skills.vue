<template>
  <section id="skills">
    <div class="container">
      <div class="section-title">
        <h1>What I Do</h1>
      </div>
    </div>
    <div class="container">
      <div class="columns">
        <div class="column card">
          <CodeIcon />
          <h2>Frontend Development</h2>
          <p>While I'm not a designer, I do love to make websites and web apps look and function smoothly and beautifully! I strive to make sites accessible with great UX.</p>
          <div class="skills-list">
            <p><span>HTML</span></p>
            <p><span>CSS</span></p>
            <p><span>LESS</span></p>
            <p class="highlighted"><span>SCSS</span></p>
            <p><span>Flexbox</span></p>
            <p class="highlighted"><span>Grid</span></p>
            <p><span>Foundation</span></p>
            <p><span>Bootstrap</span></p>
            <p><span>GULP</span></p>
            <p><span>Javascript/jQuery</span></p>
            <p><span>React</span></p>
            <p class="highlighted"><span>VUE</span></p>
          </div>
        </div>
        <div class="column card">
          <AppIcon />
          <h2>Backend Development</h2>
          <p>I'm most excited when I'm able to create a speedy API or a slick backend application. I love bringing the data to that frontend to make pretty.</p>
          <div class="skills-list">
            <p class="highlighted"><span>PHP</span></p>
            <p><span>Python</span></p>
            <p><span>C#</span></p>
            <p class="highlighted"><span>Laravel</span></p>
            <p><span>Django</span></p>
            <p class="highlighted"><span>MySQL</span></p>
            <p><span>PostgreSQL</span></p>
            <p><span>MongoDB</span></p>
            <p><span>Linux</span></p>
            <p><span>Git (Bitbucket, Github, GitLab</span></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import CodeIcon from '~/components/Icons/Code.vue'
import AppIcon from '~/components/Icons/AppDev.vue'

export default {
  name: 'Skills',
  components: {
    CodeIcon,
    AppIcon
  }
}
</script>
