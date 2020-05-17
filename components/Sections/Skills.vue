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
          <h2>Web Development</h2>
          <p>While I'm not a designer, I do love to make websites and web apps look and function smoothly 
            and beautifully! I have experience in Magento &amp; Shopify as well as Wordpress. In addition to flat 
            custom sites of course!</p>
          <div class="skills-list">
            <p> HTML</p>
            <p>CSS</p>
            <p>LESS</p>
            <p>SCSS</p>
            <p>Flexbox</p>
            <p>Foundation</p>
            <p>Bootstrap</p>
            <p>GULP</p>
            <p>Javascript/jQuery</p>
            <p>React</p>
            <p>VUE</p>
          </div>
        </div>
        <div class="column card">
          <AppIcon />
          <h2>App Development</h2>
          <p>I have moved into developing web applications and I am extremely enthusiastic about working 
            with and learning new technologies that will help expand the project possibilities.</p>
          <div class="skills-list">
            <p> PHP</p>
            <p>Python</p>
            <p>C#</p>
            <p>Laravel</p>
            <p>Django</p>
            <p>MySQL</p>
            <p>PostgreSQL</p>
            <p>MongoDB</p>
            <p>Linux</p>
            <p>Git (Bitbucket, Github, GitLab</p>
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
