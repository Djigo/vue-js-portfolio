<template>
  <div id="contact" class="contact section">
    <div class="cover">
    <h1>Contact</h1>
    <Navbar/>
    <div class="middle-anchor" v-view></div>
    </div>
    <div class="content">
  <p>
Kaya Warwaru 96<br>
Curacao<br>
+5999 5234902<br>
info@acacia.com
</p>
    </div>
    <div class="upper-anchor" v-view="upperAnchorHandler"></div>
    <div class="lower-anchor" v-view="lowerAnchorHandler"></div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
    name: 'Contact',
    components:{
      Navbar
    }, 
    methods: {
    upperAnchorHandler(e) {
      //Scrolling up
      if (e.scrollValue < 0) {
        if (e.type === "enter") {
          this.stickyAbout = false;
          this.stickyAboutBottom = false;
          
        }
      }
      //Scrolling down
      if (e.scrollValue > 0 && e.scrollValue < 500) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
          this.$router.push('#contact')
        }
      }
    },
    //middleAnchorHandler(e) {

    //},

    lowerAnchorHandler(e) {
      //Scrolling up
      if (e.scrollValue < 0) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
          this.$router.push('#contact')
        }
      }
      //Scrolling down
      if (e.scrollValue > 0) {
        if (e.type === "enter") {
          this.stickyAbout = false;
          this.stickyAboutBottom = true;
        }
      }
    }
    
  }
}
</script>

<style lang="scss">

.contact {
  position: relative;
  min-height: 100vh;
  .cover {
    padding: 10px;
    height: 100vh;
    min-height: 100vh;
    background:#E5855E;
    color:#fff;
    position: relative;
    -webkit-transition: width 0.2s; /* Safari */
    transition: width 0.2s;
     -webkit-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.10);
-moz-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.10);
box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.10);
  }
  .nav {
    position: absolute;
    bottom: 0px;
    li {
      a {
        color: #fff;
        &.router-link-exact-active {
          border-bottom: 3px solid #fff;
        }
      }
    }
  }
  .content {
    padding-top: 5px;
    min-height:100vh;
    position: relative;
    display: flex;
    -webkit-box-align: center;
        align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    p{
      vertical-align: middle;
      text-align: center;
    }
  }
  .upper-anchor {
    width: 10px;
    height: 1px;
    position: absolute;
    background: pink;
    z-index: 2000;
    left: 0px;
    top: -1px;
    opacity: 1;
  }
  .middle-anchor {
    width: 10px;
    height: 1px;
    position: absolute;
    background: pink;
    z-index: 2000;
    left: 0px;
    bottom: -1px;
    opacity: 1;
  }
  .lower-anchor {
    width: 10px;
    height: 1px;
    position: absolute;
    background: black;
    z-index: 2000;
    left: 0px;
    bottom: -1px;
    opacity: 1;
  }
}

@media only screen and (min-width: 992px) {
  .contact {
    .cover {
      width: 50%;
      position: absolute;
      top: 0px;
      bottom: auto;
      &.sticky {
        position: fixed;
        top: 0px;
        bottom: auto;
        margin-top:0px;
      }
      &.sticky-bottom {
        top: auto;
        bottom: 0px;
        height: 100vh;
        position: absolute;
      }
    }
    .content {
      padding-left: 50%;
      position: relative;
    }
  }
}

</style>
