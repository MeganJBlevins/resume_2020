<template>
  <nav id="nav" class="navbar" role="navigation" aria-label="main navigation">
    <div class="navigation__container">
      <div class="navbar-brand">
        <a class="navbar-item" href="#about">
          <img src="images/MB_Logo.png" alt="Logo"/>
        </a>

        <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" @click="showMobileNav()">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div class="navbar-menu">
        <div class="navbar-start">
          <nuxt-link 
            class="navbar-item"
            :to="{ path: '/',hash:'#about'}"
          >
            About
          </nuxt-link>
          <nuxt-link 
            class="navbar-item"
            :to="{ path: '/',hash:'#skills'}"
          >
            Skills
          </nuxt-link>
          <nuxt-link 
            class="navbar-item"
            :to="{ path: '/',hash:'#experience'}"
          >
            Experience
          </nuxt-link>
          <nuxt-link 
            class="navbar-item"
            :to="{ path: '/',hash:'#portfolio'}"
          >
            Portfolio
          </nuxt-link>
          <nuxt-link 
            class="navbar-item"
            :to="{ path: '/',hash:'#contact'}"
          >
            Contact
          </nuxt-link>
        </div>
      </div>
      <transition name="slide-fade">
        <div 
          class="mobile-nav__overlay"
          @click.self="closeMobileNav"
          v-if="this.mobileNav"
        >
          <div class="mobile-nav__container" >
            <div class="mobile-nav">
              <nuxt-link 
              class="navbar-item__mobile navbar-item"
              :to="{ path: '/',hash:'#about'}"
              @click="closeMobileNav"
            >
              About
            </nuxt-link>
            <nuxt-link 
              class="navbar-item__mobile navbar-item"
              :to="{ path: '/',hash:'#skills'}"
            >
              Skills
            </nuxt-link>
            <nuxt-link 
              class="navbar-item__mobile navbar-item"
              :to="{ path: '/',hash:'#experience'}"
            >
              Experience
            </nuxt-link>
            <nuxt-link 
              class="navbar-item__mobile navbar-item"
              :to="{ path: '/',hash:'#portfolio'}"
            >
              Portfolio
            </nuxt-link>
            <nuxt-link 
              class="navbar-item__mobile navbar-item"
              :to="{ path: '/',hash:'#contact'}"
            >
              Contact
            </nuxt-link>
            </div>
          </div>
        </div>
      </transition>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
   data() {
     return {
        windowTop: 0,
        mobileNav: false
     }
  },
  mounted() {
      this.$nextTick(function(){
        window.addEventListener("scroll", function(){
          var navbar = document.getElementById("nav");
          var nav_classes = navbar.classList;
          if(document.documentElement.scrollTop >= 150) {
            if (nav_classes.contains("fixed") === false) {
              nav_classes.toggle("fixed");
            }
          }
          else {
            if (nav_classes.contains("fixed") === true) {
              nav_classes.toggle("fixed");
            }
          }
        })
      })
    },
  watch: {
    '$route' () {
      this.mobileNav = false;
    }
  },
  methods: {
    showMobileNav() {
      this.mobileNav = true;
    },
    closeMobileNav() {
      this.mobileNav = false;
    }
  }
}
</script>

<style lang="scss">


</style>