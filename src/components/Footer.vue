<template>
  <div class="footer section" v-view>
    <video autoplay muted loop id="myVideo">
  <source src="../assets/videos/intro.mp4" type="video/mp4">
</video>
    <div class="cover">
      <div class="circle"></div>
    <h1>Footer Animation</h1>
    <parallax :speed-factor="0.3">
  <img src="https://images.pexels.com/photos/132037/pexels-photo-132037.jpeg">
</parallax>
    <Navbar/>
    </div>
  </div>
</template>

<script>
import Parallax from "vue-parallaxy";
import Navbar from '@/components/Navbar.vue'
export default {
    name: 'Footer',
    components:{
      Parallax, Navbar
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
      if (e.scrollValue > 0) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
        }
      }
    },
    //middleAnchorHandler(e) {},

    lowerAnchorHandler(e) {
      //Scrolling up
      if (e.scrollValue < 0) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
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

.footer {
  position: relative;
  background:#011838;
  video{
  position:absolute;
  z-index:0;
  height:120vh;
  opacity:0.5;
}
  .cover {
    padding: 10px;
    height: 100vh;
    color:#fff;
    position: relative;
    -webkit-transition: width 0.2s; /* Safari */
    transition: width 0.2s;
    z-index:1;
    .circle{
      width: 40vh;
      height: 40vh;
      position:absolute;
      z-index:-1;
      background:#BA8477;
    }
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
    position: relative;
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

.footer .cover #nav a{
  color:#fff;
}

</style>