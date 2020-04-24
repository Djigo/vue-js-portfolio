<template>
  <div id="work" class="work section" v-view>
    <div class="cover" v-bind:class="{ 'sticky': stickyAbout, 'sticky-bottom': stickyAboutBottom  }" ref="coverWork">
      <h1>Work</h1>
      <Navbar/>
      <div class="middle-anchor" v-view></div>
    </div>
    <div class="content">
      <Project1/>
    </div>
    <div class="upper-anchor" v-view="upperAnchorHandler"></div>
    <div class="lower-anchor" v-view="lowerAnchorHandler"></div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Project1 from "@/components/Project1.vue";

export default {
  name: "Work",
  components: {
    Navbar,
    Project1
  },
  props: [],
  data() {
    return {
      stickyAbout: false,
      stickyAboutBottom: false,
      bounding: null
    };
  },
  methods: {
    upperAnchorHandler(e) {
      //Scrolling up
      if (e.scrollValue < 0 && e.scrollValue > -500) {
        if (e.type === "enter") {
          this.stickyAbout = false;
          this.stickyAboutBottom = false;
          this.$router.push('#work')
        }
      }
      //Scrolling down
      
      if (e.scrollValue > 0 && e.scrollValue < 500) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
          this.$router.push('#work')
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
};
</script>

<style lang="scss">

.work {
  background:#fff;
  position: relative;
  .cover {
    padding: 10px;
    height: 100vh;
    min-height: 100vh;
    background:#fff;
    position: relative;
    -webkit-transition: width 0.2s; /* Safari */
    transition: width 0.2s;
    -webkit-transform:translate3d(0,0,0);
    transform:translate3d(0,0,0);
    transform:translate3d(0,0,0);
     -webkit-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.05);
-moz-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.05);
box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.05);
  }
  .nav {
    position: absolute;
    bottom: 0px;
    li {
      a {
        color: #E5855E;
        &.router-link-exact-active {
          border-bottom: 3px solid #E5855E;
        }
      }
    }
  }
  .content {
    padding-top: 0px;
    position: relative;
    .showcase{
      position:relative;
      height:100vh;
      img{
        display:block;
      }
      .description{
        vertical-align: middle;
        width:100%;
        position:absolute;
        top:40%;
        color:#fff;
      }
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
    bottom: 50%;
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
  .work {
    min-height: 100vh;
    .cover {
      width: 50%;
      position: absolute;
      top: 0px;
      bottom: auto;
      &.sticky {
        position: fixed;
        top: 0px;
        bottom: auto;
        margin-top: 0px;
        height: 100vh;
      }
      &.sticky-bottom {
        top: auto;
        bottom: 0px;
        height: 100vh;
        position: absolute;
      }
    }
    .content {
      margin-left: 50%;
    }
  }
}

</style>
