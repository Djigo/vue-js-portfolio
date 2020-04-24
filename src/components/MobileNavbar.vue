<template>
  <div class="mobile-navbar">
    <div class="hexagon frame" @click="toggleBurger" v-bind:class="{ open: isOpen }">
      <div class="hex-outer h1"></div>
      <div class="hex-outer h2"></div>
      <div class="hex-outer h3"></div>
      <div class="hex-inner h1"></div>
      <div class="hex-inner h2"></div>
      <div class="hex-inner h3"></div>
      <div class="label">
        <div class="nav-icon1" id="nav-icon1" v-bind:class="{ open: isOpen }">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
    <div v-if="(this.isOpen)" class="mobile-navbar-list">
      <ul class="center-align">
        <li @click="toggleBurger">
          <router-link to="/">Home</router-link>
        </li>
        <li @click="toggleBurger">
          <router-link to="#about">About</router-link>
        </li>
        <li @click="toggleBurger">
          <router-link to="#work">Work</router-link>
        </li>
        <li @click="toggleBurger">
          <router-link to="#contact">Contact</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileNavbar",
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleBurger() {
      this.isOpen = !this.isOpen;
      if (this.isOpen) {
        document.documentElement.style.overflow = "hidden";
        document.body.scroll = "no";
      } else {
        document.documentElement.style.overflow = "scroll";
        document.body.scroll = "yes";
      }
    }
  }
};
</script>

<style lang="scss">
.mobile-navbar {
  z-index: 9999;
  position: fixed;
  li {
    display: block;
    cursor: pointer;
    a {
      text-transform: uppercase;
      font-weight: bold;
      color: #e5855e;
      padding: 5px;
      &.router-link-exact-active {
        border-bottom: 3px solid white;
      }
    }
  }
  .frame {
    width: 60px;
    height: 50px;
    left: 5px;
    margin: 0;
    margin-top: 0px;
    position: fixed;
    cursor: pointer;
    -ms-transform: scale(0.18, 0.18); /* IE 9 */
    -webkit-transform: scale(0.18, 0.18); /* Safari */
    transform: scale(0.18, 0.18);
    z-index: 1000;
    &:hover {
      -ms-transform: scale(0.19); /* IE 9 */
    -webkit-transform: scale(0.19); /* Safari */
    transform: scale(0.19);
    left:4px;
    top:-1px;
      .label {
        transform: scale(1);
        -webkit-transform: scale(1);
      }
    }
    .hex-outer {
      width: 210px;
      height: 120px;
      border-top: 105px solid #BA8377;
      border-left: 60px solid transparent;
      &.h1 {
        position: absolute;
        top: 80px;
        -webkit-transition: all 0.3s; /* Safari */
        transition: all 0.5s;
        -webkit-transform: rotateZ(0deg);
        -ms-transform: rotateZ(0deg);
        transform: rotateZ(0deg);
      }
      &.h2 {
        position: absolute;
        top: 80px;
        transform: rotate(60deg);
        -webkit-transform: rotate(60deg);
      }
      &.h3 {
        position: absolute;
        top: 80px;
        transform: rotate(-60deg);
        -webkit-transform: rotate(-60deg);
      }
    }
    .hex-inner {
      background: #BA8377;
      width: 200px;
      height: 115px;
      border-top: 100px solid #BA8377;
      border-left: 210px solid transparent;
      position: relative;
      left: 0px;
      top: 82px !important;
      transition: all 0.4s;
      -webkit-transition: all 0.4s;
      &.h1 {
        position: absolute;
        top: 80px;
        -webkit-transition: all 0.3s; /* Safari */
        transition: all 0.5s;
        -webkit-transform: rotateZ(0deg);
        -ms-transform: rotateZ(0deg);
        transform: rotateZ(0deg);
      }
      &.h2 {
        position: absolute;
        top: 80px;
        transform: rotate(60deg);
        -webkit-transform: rotate(60deg);
      }
      &.h3 {
        position: absolute;
        top: 80px;
        transform: rotate(-60deg);
        -webkit-transform: rotate(-60deg);
      }
    }
    &.open {
      .h1 {
        -webkit-transition: all 0.05s; /* Safari */
        transition: all 0.5s;
        -webkit-transform: rotateZ(-180deg);
        -ms-transform: rotateZ(-180deg);
        transform: rotateZ(-180deg);
      }
      .h2 {
        transition-delay: 1s;
        -webkit-transition: all 0.5s; /* Safari */
        transition: all 0.5s;
        -webkit-transform: rotateZ(-240deg);
        -ms-transform: rotateZ(-240deg);
        transform: rotateZ(-240deg);
      }
      .h3 {
        transition-delay: 1s;
        -webkit-transition: all 0.5s; /* Safari */
        transition: all 0.5s;
        -webkit-transform: rotateZ(-300deg);
        -ms-transform: rotateZ(-300deg);
        transform: rotateZ(-300deg);
      }
    }
    .label {
      position: absolute;
      color: #abf8ff;
      font-weight: bold;
      font-size: 160px;
      left: 59px;
      top: 36px;
      /* Icon 1 */
      * {
        margin: 0;
        padding: 0;
      }

      /* Icons */

      #nav-icon1,
      #nav-icon2,
      #nav-icon3,
      #nav-icon4 {
        
        width: 60px;
        height: 45px;
        position: relative;
        top: 30px;
        left: 11px;
        margin: 50px auto;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: 0.5s ease-in-out;
        -moz-transition: 0.5s ease-in-out;
        -o-transition: 0.5s ease-in-out;
        transition: 0.5s ease-in-out;
        cursor: pointer;
        transform: scale(2);
        -webkit-transform: scale(2);
      }

      #nav-icon1 span,
      #nav-icon3 span,
      #nav-icon4 span {
        display: block;
        position: absolute;
        height: 9px;
        width: 100%;
        background: #fff;
        opacity: 1;
        left: 0;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: 0.25s ease-in-out;
        -moz-transition: 0.25s ease-in-out;
        -o-transition: 0.25s ease-in-out;
        transition: 0.25s ease-in-out;
        
      }

      #nav-icon1 span:nth-child(1) {
        top: 0px;
      }

      #nav-icon1 span:nth-child(2) {
        top: 18px;
      }

      #nav-icon1 span:nth-child(3) {
        top: 36px;
      }

      #nav-icon1.open span:nth-child(1) {
        top: 18px;
        -webkit-transform: rotate(135deg);
        -moz-transform: rotate(135deg);
        -o-transform: rotate(135deg);
        transform: rotate(135deg);
      }

      #nav-icon1.open span:nth-child(2) {
        opacity: 0;
        left: -60px;
      }

      #nav-icon1.open span:nth-child(3) {
        top: 18px;
        -webkit-transform: rotate(-135deg);
        -moz-transform: rotate(-135deg);
        -o-transform: rotate(-135deg);
        transform: rotate(-135deg);
      }

      /* Icon 2 */

      #nav-icon2 {
      }

      #nav-icon2 span {
        display: block;
        position: absolute;
        height: 9px;
        width: 50%;
        background: #d3531a;
        opacity: 1;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: 0.25s ease-in-out;
        -moz-transition: 0.25s ease-in-out;
        -o-transition: 0.25s ease-in-out;
        transition: 0.25s ease-in-out;
      }

      #nav-icon2 span:nth-child(even) {
        left: 50%;
      }

      #nav-icon2 span:nth-child(odd) {
        left: 0px;
      }

      #nav-icon2 span:nth-child(1),
      #nav-icon2 span:nth-child(2) {
        top: 0px;
      }

      #nav-icon2 span:nth-child(3),
      #nav-icon2 span:nth-child(4) {
        top: 18px;
      }

      #nav-icon2 span:nth-child(5),
      #nav-icon2 span:nth-child(6) {
        top: 36px;
      }

      #nav-icon2.open span:nth-child(1),
      #nav-icon2.open span:nth-child(6) {
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        transform: rotate(45deg);
      }

      #nav-icon2.open span:nth-child(2),
      #nav-icon2.open span:nth-child(5) {
        -webkit-transform: rotate(-45deg);
        -moz-transform: rotate(-45deg);
        -o-transform: rotate(-45deg);
        transform: rotate(-45deg);
      }

      #nav-icon2.open span:nth-child(1) {
        left: 5px;
        top: 7px;
      }

      #nav-icon2.open span:nth-child(2) {
        left: calc(50% - 5px);
        top: 7px;
      }

      #nav-icon2.open span:nth-child(3) {
        left: -50%;
        opacity: 0;
      }

      #nav-icon2.open span:nth-child(4) {
        left: 100%;
        opacity: 0;
      }

      #nav-icon2.open span:nth-child(5) {
        left: 5px;
        top: 29px;
      }

      #nav-icon2.open span:nth-child(6) {
        left: calc(50% - 5px);
        top: 29px;
      }

      /* Icon 3 */

      #nav-icon3 span:nth-child(1) {
        top: 0px;
      }

      #nav-icon3 span:nth-child(2),
      #nav-icon3 span:nth-child(3) {
        top: 18px;
      }

      #nav-icon3 span:nth-child(4) {
        top: 36px;
      }

      #nav-icon3.open span:nth-child(1) {
        top: 18px;
        width: 0%;
        left: 50%;
      }

      #nav-icon3.open span:nth-child(2) {
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        transform: rotate(45deg);
      }

      #nav-icon3.open span:nth-child(3) {
        -webkit-transform: rotate(-45deg);
        -moz-transform: rotate(-45deg);
        -o-transform: rotate(-45deg);
        transform: rotate(-45deg);
      }

      #nav-icon3.open span:nth-child(4) {
        top: 18px;
        width: 0%;
        left: 50%;
      }

      /* Icon 4 */

      #nav-icon4 {
      }

      #nav-icon4 span:nth-child(1) {
        top: 0px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4 span:nth-child(2) {
        top: 18px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4 span:nth-child(3) {
        top: 36px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4.open span:nth-child(1) {
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        transform: rotate(45deg);
        top: -3px;
        left: 8px;
      }

      #nav-icon4.open span:nth-child(2) {
        width: 0%;
        opacity: 0;
      }

      #nav-icon4.open span:nth-child(3) {
        -webkit-transform: rotate(-45deg);
        -moz-transform: rotate(-45deg);
        -o-transform: rotate(-45deg);
        transform: rotate(-45deg);
        top: 39px;
        left: 8px;
      }
    }
  }
  .mobile-navbar-list {
    background: #fff;
    position: fixed;
    width: 100vw;
    height: 100vh;
    z-index: 999;
    display: flex;
    align-items: center; /* horizontal */
    justify-content: center; /* vertical */
    ul {
      width: 100vw;
      li {
        padding: 30px 0px;
      }
    }
  }
}

@media only screen and (min-width: 992px) {
    .mobile-navbar{
      display:none;
    }
  }
</style>