<template>
  <div class="nav">
    <ul>
      <li v-scroll-to="'#intro'">
        <router-link to="/">Home</router-link>|
      </li>
      <li v-scroll-to="'#about'">
        <router-link to="#about">About</router-link>|
      </li>
      <li v-scroll-to="'#work'">
        <router-link to="#work">Work</router-link>|
      </li>
      <li v-scroll-to="'#contact'">
        <router-link to="#contact">Contact</router-link>
      </li>
    </ul>
    <router-view/>
  </div>
</template>

<script>

export default {
  name: "Navbar",
  data() {
    return {
    };
  },
  components: {
    // VueScrollTo
  },
  methods: {
    //test(el) {
      //console.log(el)
      //VueScrollTo.scrollTo(el);
    //}
  }
};
</script>

<style lang="scss" scoped>
  .nav {
    padding: 30px;
    color: #dc5924;
    display:none;
    li {
      display: inline-block;
      a {
        text-transform: uppercase;
        font-weight: bold;
        color: #fff;
        padding: 5px;
        &.router-link-exact-active {
          border-bottom: 3px solid white;
        }
      }
    }
  }
  .intro{
    .nav{
      display:block;
    }
  }

  @media only screen and (min-width: 992px) {
    .nav{
      display:block;
    }
  }

  
</style>