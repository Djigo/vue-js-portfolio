<template>
  <div class="home page">
    <MobileNavbar/>
    <Intro msg="Welcome to Your Vue.js App"> </Intro>
    <About></About>
    <Work></Work>
    <Contact/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import MobileNavbar from '@/components/MobileNavbar.vue'
import Intro from '@/components/Intro.vue'
import About from '@/components/About.vue'
import Work from '@/components/Work.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    MobileNavbar, Intro, About, Work, Contact, Footer
  },
  data(){
        return {
        
        }
    },
    methods:{
    
    }
}
</script>

<style lang="scss">
.section{
  margin:0;
  padding: 0 0 0 0;
  min-height:100vh;
  overflow:hidden;
 .container{
   padding-bottom:70px;
   overflow: hidden;
 }
}
  .cover{
    display: flex;
    align-items: center; /* horizontal */
    justify-content: center; /* vertical */
    height:100vh;
    position: relative;
    overflow:hidden;
    z-index: 1000;
    h1{
    font-family: 'Caveat', cursive;
    }
    .nav{
    position:absolute;
    bottom:0px;
    }
  }
  .content{
    min-height:100vh;
  }
</style>

