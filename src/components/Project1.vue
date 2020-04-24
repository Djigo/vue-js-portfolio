<template>
<div class="project">
  <div class="project1" 
  v-bind:class="{ 'open': projectOpen === 1 }">
    <div
      id="showcase1"
      v-scroll-to="{ element: '#showcase1', duration: 2000 }"
      class="showcase"
      v-bind:class="{ 'open': projectOpen === 1 }"
      @click="projectToggle(1)"
    >
      <img src="../assets/images/cover1.jpg">
      <div class="description">
        <h2>Title</h2>
        <h3>Subtitle</h3>
        <div class="circle">

          <div class="label">
            <div class="showmore" v-if="projectOpen !== 1">
            <span>MORE</span>
            <div class="arrow"></div>
            </div>
            <div class="showless" v-if="projectOpen === 1">
            <i class="material-icons close">close</i>
            </div>
          </div>
        </div>
      </div>
    </div>

    
    <div class="showcase-content" v-bind:class="{ 'open': projectOpen === 1 }">
      <div class="container">
<h2>Core investment banking activities</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris lacinia erat sapien, molestie varius ipsum euismod tincidunt. In lorem ante, imperdiet sed tincidunt ut, malesuada hendrerit ante. Vivamus elementum est et arcu sagittis, sed varius arcu iaculis. Suspendisse varius ex non pharetra ultricies. Donec feugiat diam luctus quam varius, vitae consequat ante finibus. Morbi euismod risus eu tellus dapibus pellentesque at vitae dui. Cras laoreet ipsum sit amet nibh ornare, ac placerat enim egestas. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Curabitur cursus sed ex id vulputate. Cras luctus justo eget ante malesuada consequat. Suspendisse potenti. Nullam varius risus augue, luctus aliquam massa commodo in. Quisque sed felis auctor, accumsan risus in, placerat metus. Nulla ac augue interdum, facilisis nisl id, ornare sapien. Mauris malesuada elementum nibh, vel consequat enim aliquet quis.</p>

      <p>Proin suscipit vehicula dolor, maximus accumsan libero sodales eu. Ut fermentum posuere leo, sit amet ultricies libero laoreet quis. Nunc vel metus sapien. Mauris imperdiet fringilla congue. Donec quam urna, placerat eu commodo vel, tincidunt vitae augue. Duis vestibulum, eros quis pulvinar aliquet, sem nisl ullamcorper velit, sit amet pellentesque lacus tellus vitae ligula. Sed ultricies lectus in ante tristique luctus. Nulla lacinia nibh at lorem bibendum, at tristique lorem fermentum. Nam ac est in nulla cursus commodo. Suspendisse sodales neque eros, nec placerat sapien ornare sed. Curabitur quis commodo libero. Pellentesque erat mi, lobortis eget aliquet vitae, tempus posuere elit. Ut vitae fermentum mi, id fringilla lorem.</p>

      <p>Integer dignissim vitae magna nec laoreet. Vivamus varius purus nec cursus pretium. Morbi tincidunt enim ut efficitur vestibulum. Nam luctus auctor nunc, sed volutpat magna vestibulum vel. Aenean ac mauris placerat, scelerisque turpis in, hendrerit odio. Etiam hendrerit ipsum sit amet ex commodo, eget pulvinar nulla ullamcorper. Integer quis fermentum velit. Pellentesque pellentesque leo eu nunc pulvinar pulvinar.</p>

      <p>Maecenas accumsan vel nunc a vestibulum. Integer sit amet ligula id quam bibendum rutrum ac eu nisi. Nam tempus purus orci, sit amet lobortis diam ultrices convallis. Morbi sit amet laoreet mauris, eget pharetra nulla. Aliquam tempor ligula eget tortor pellentesque, et sollicitudin leo viverra. Donec consectetur ultrices eros ac commodo. Mauris non accumsan eros, nec rutrum risus. Sed purus odio, fermentum a massa ut, mollis tempus mi. Nam suscipit congue fringilla.</p>

      <p>Vestibulum non ex ullamcorper, facilisis libero volutpat, dapibus arcu. Maecenas placerat leo quis mollis cursus. Proin eu tristique leo, ut consectetur elit. Integer vel tincidunt lacus. Vivamus tempor quam at nulla varius, et molestie urna semper. Suspendisse potenti. Cras in nibh vitae velit pretium dignissim eu id massa. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.</p>

      <p>Curabitur tincidunt porttitor pretium. Vivamus consequat odio et libero venenatis, et gravida nisi elementum. Integer tristique turpis faucibus neque commodo, non efficitur turpis lobortis. Proin vehicula et metus sed sodales. Ut quis condimentum augue. Maecenas tempus lorem ligula. Nullam rutrum dui in placerat suscipit. Aliquam a dapibus purus. Nulla enim ante, cursus non urna vel, egestas ullamcorper felis. Nullam laoreet orci turpis, vitae efficitur lacus pulvinar sagittis. Nam justo ipsum, rutrum non accumsan sed, molestie eu purus. Curabitur imperdiet nisl sed mi varius, in accumsan purus dignissim. Phasellus consequat sollicitudin massa, et rutrum arcu feugiat ut. Pellentesque lacus arcu, volutpat nec nisi vel, commodo finibus orci.</p>

      <p>Nulla cursus sem id dolor sagittis, sit amet hendrerit risus tristique. Nunc mattis condimentum enim, ut commodo mi sodales aliquam. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum nibh mi, pellentesque eget lacus in, condimentum condimentum nibh. Sed non porta augue. Etiam dictum ullamcorper sem at tristique. Curabitur ullamcorper nunc sed laoreet elementum. Vivamus volutpat consectetur nibh at dictum. Curabitur dictum est non ultrices varius. Aliquam a orci cursus, vestibulum augue ac, luctus ante. Praesent lobortis nibh in tellus accumsan, vitae pretium neque sollicitudin.</p>
    </div>
    </div>
    </div>
    <div class="project1" 
    v-bind:class="{ 'open': projectOpen === 2 }">
    <div
      id="showcase2"
      v-scroll-to="{ element: '#showcase2', duration: 1000 }"
      class="showcase"
      v-bind:class="{ 'open': projectOpen === 2 }"
      @click="projectToggle(2)"
    >
      <img src="../assets/images/cover2.jpg">
      <div class="description">
        <h2>Title</h2>
        <h3>Subtitle</h3>
        <div class="circle">

          <div class="label">
            <div class="showmore" v-if="projectOpen !== 2" >
            <span>MORE</span>
            <div class="arrow"></div>
            </div>
            <div class="showless" v-if="projectOpen === 2">
            <i class="material-icons close">close</i>
            </div>
          </div>
        </div>
      </div>
    </div>

    
    <div class="showcase-content" v-bind:class="{ 'open': projectOpen === 2 }">
      <div class="container">
        <h2>Core investment banking activities</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris lacinia erat sapien, molestie varius ipsum euismod tincidunt. In lorem ante, imperdiet sed tincidunt ut, malesuada hendrerit ante. Vivamus elementum est et arcu sagittis, sed varius arcu iaculis. Suspendisse varius ex non pharetra ultricies. Donec feugiat diam luctus quam varius, vitae consequat ante finibus. Morbi euismod risus eu tellus dapibus pellentesque at vitae dui. Cras laoreet ipsum sit amet nibh ornare, ac placerat enim egestas. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Curabitur cursus sed ex id vulputate. Cras luctus justo eget ante malesuada consequat. Suspendisse potenti. Nullam varius risus augue, luctus aliquam massa commodo in. Quisque sed felis auctor, accumsan risus in, placerat metus. Nulla ac augue interdum, facilisis nisl id, ornare sapien. Mauris malesuada elementum nibh, vel consequat enim aliquet quis.</p>

      <p>Proin suscipit vehicula dolor, maximus accumsan libero sodales eu. Ut fermentum posuere leo, sit amet ultricies libero laoreet quis. Nunc vel metus sapien. Mauris imperdiet fringilla congue. Donec quam urna, placerat eu commodo vel, tincidunt vitae augue. Duis vestibulum, eros quis pulvinar aliquet, sem nisl ullamcorper velit, sit amet pellentesque lacus tellus vitae ligula. Sed ultricies lectus in ante tristique luctus. Nulla lacinia nibh at lorem bibendum, at tristique lorem fermentum. Nam ac est in nulla cursus commodo. Suspendisse sodales neque eros, nec placerat sapien ornare sed. Curabitur quis commodo libero. Pellentesque erat mi, lobortis eget aliquet vitae, tempus posuere elit. Ut vitae fermentum mi, id fringilla lorem.</p>

      <p>Integer dignissim vitae magna nec laoreet. Vivamus varius purus nec cursus pretium. Morbi tincidunt enim ut efficitur vestibulum. Nam luctus auctor nunc, sed volutpat magna vestibulum vel. Aenean ac mauris placerat, scelerisque turpis in, hendrerit odio. Etiam hendrerit ipsum sit amet ex commodo, eget pulvinar nulla ullamcorper. Integer quis fermentum velit. Pellentesque pellentesque leo eu nunc pulvinar pulvinar.</p>

      <p>Maecenas accumsan vel nunc a vestibulum. Integer sit amet ligula id quam bibendum rutrum ac eu nisi. Nam tempus purus orci, sit amet lobortis diam ultrices convallis. Morbi sit amet laoreet mauris, eget pharetra nulla. Aliquam tempor ligula eget tortor pellentesque, et sollicitudin leo viverra. Donec consectetur ultrices eros ac commodo. Mauris non accumsan eros, nec rutrum risus. Sed purus odio, fermentum a massa ut, mollis tempus mi. Nam suscipit congue fringilla.</p>

      <p>Vestibulum non ex ullamcorper, facilisis libero volutpat, dapibus arcu. Maecenas placerat leo quis mollis cursus. Proin eu tristique leo, ut consectetur elit. Integer vel tincidunt lacus. Vivamus tempor quam at nulla varius, et molestie urna semper. Suspendisse potenti. Cras in nibh vitae velit pretium dignissim eu id massa. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.</p>

      <p>Curabitur tincidunt porttitor pretium. Vivamus consequat odio et libero venenatis, et gravida nisi elementum. Integer tristique turpis faucibus neque commodo, non efficitur turpis lobortis. Proin vehicula et metus sed sodales. Ut quis condimentum augue. Maecenas tempus lorem ligula. Nullam rutrum dui in placerat suscipit. Aliquam a dapibus purus. Nulla enim ante, cursus non urna vel, egestas ullamcorper felis. Nullam laoreet orci turpis, vitae efficitur lacus pulvinar sagittis. Nam justo ipsum, rutrum non accumsan sed, molestie eu purus. Curabitur imperdiet nisl sed mi varius, in accumsan purus dignissim. Phasellus consequat sollicitudin massa, et rutrum arcu feugiat ut. Pellentesque lacus arcu, volutpat nec nisi vel, commodo finibus orci.</p>

      <p>Nulla cursus sem id dolor sagittis, sit amet hendrerit risus tristique. Nunc mattis condimentum enim, ut commodo mi sodales aliquam. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum nibh mi, pellentesque eget lacus in, condimentum condimentum nibh. Sed non porta augue. Etiam dictum ullamcorper sem at tristique. Curabitur ullamcorper nunc sed laoreet elementum. Vivamus volutpat consectetur nibh at dictum. Curabitur dictum est non ultrices varius. Aliquam a orci cursus, vestibulum augue ac, luctus ante. Praesent lobortis nibh in tellus accumsan, vitae pretium neque sollicitudin.</p>
    </div>
    </div>
    </div>
    <div class="project1" 
    v-bind:class="{ 'open': projectOpen === 3 }">
    <div
      id="showcase3"
      v-scroll-to="{ element: '#showcase3', duration: 1000 }"
      class="showcase"
      v-bind:class="{ 'open': projectOpen === 3 }"
      @click="projectToggle(3)"
    >
      <img src="../assets/images/cover3.jpg">
      <div class="description">
        <h2>Title</h2>
        <h3>Subtitle</h3>
        <div class="circle">

          <div class="label">
            <div class="showmore" v-if="projectOpen !== 3">
            <span>MORE</span>
            <div class="arrow"></div>
            </div>
            <div class="showless" v-if="projectOpen === 3">
            <i class="material-icons close">close</i>
            </div>
          </div>
        </div>
      </div>
    </div>

    
    <div class="showcase-content" v-bind:class="{ 'open': projectOpen === 3 }">
      <div class="container">
        <h2>Core investment banking activities</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris lacinia erat sapien, molestie varius ipsum euismod tincidunt. In lorem ante, imperdiet sed tincidunt ut, malesuada hendrerit ante. Vivamus elementum est et arcu sagittis, sed varius arcu iaculis. Suspendisse varius ex non pharetra ultricies. Donec feugiat diam luctus quam varius, vitae consequat ante finibus. Morbi euismod risus eu tellus dapibus pellentesque at vitae dui. Cras laoreet ipsum sit amet nibh ornare, ac placerat enim egestas. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Curabitur cursus sed ex id vulputate. Cras luctus justo eget ante malesuada consequat. Suspendisse potenti. Nullam varius risus augue, luctus aliquam massa commodo in. Quisque sed felis auctor, accumsan risus in, placerat metus. Nulla ac augue interdum, facilisis nisl id, ornare sapien. Mauris malesuada elementum nibh, vel consequat enim aliquet quis.</p>

      <p>Proin suscipit vehicula dolor, maximus accumsan libero sodales eu. Ut fermentum posuere leo, sit amet ultricies libero laoreet quis. Nunc vel metus sapien. Mauris imperdiet fringilla congue. Donec quam urna, placerat eu commodo vel, tincidunt vitae augue. Duis vestibulum, eros quis pulvinar aliquet, sem nisl ullamcorper velit, sit amet pellentesque lacus tellus vitae ligula. Sed ultricies lectus in ante tristique luctus. Nulla lacinia nibh at lorem bibendum, at tristique lorem fermentum. Nam ac est in nulla cursus commodo. Suspendisse sodales neque eros, nec placerat sapien ornare sed. Curabitur quis commodo libero. Pellentesque erat mi, lobortis eget aliquet vitae, tempus posuere elit. Ut vitae fermentum mi, id fringilla lorem.</p>

      <p>Integer dignissim vitae magna nec laoreet. Vivamus varius purus nec cursus pretium. Morbi tincidunt enim ut efficitur vestibulum. Nam luctus auctor nunc, sed volutpat magna vestibulum vel. Aenean ac mauris placerat, scelerisque turpis in, hendrerit odio. Etiam hendrerit ipsum sit amet ex commodo, eget pulvinar nulla ullamcorper. Integer quis fermentum velit. Pellentesque pellentesque leo eu nunc pulvinar pulvinar.</p>

      <p>Maecenas accumsan vel nunc a vestibulum. Integer sit amet ligula id quam bibendum rutrum ac eu nisi. Nam tempus purus orci, sit amet lobortis diam ultrices convallis. Morbi sit amet laoreet mauris, eget pharetra nulla. Aliquam tempor ligula eget tortor pellentesque, et sollicitudin leo viverra. Donec consectetur ultrices eros ac commodo. Mauris non accumsan eros, nec rutrum risus. Sed purus odio, fermentum a massa ut, mollis tempus mi. Nam suscipit congue fringilla.</p>

      <p>Vestibulum non ex ullamcorper, facilisis libero volutpat, dapibus arcu. Maecenas placerat leo quis mollis cursus. Proin eu tristique leo, ut consectetur elit. Integer vel tincidunt lacus. Vivamus tempor quam at nulla varius, et molestie urna semper. Suspendisse potenti. Cras in nibh vitae velit pretium dignissim eu id massa. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.</p>

      <p>Curabitur tincidunt porttitor pretium. Vivamus consequat odio et libero venenatis, et gravida nisi elementum. Integer tristique turpis faucibus neque commodo, non efficitur turpis lobortis. Proin vehicula et metus sed sodales. Ut quis condimentum augue. Maecenas tempus lorem ligula. Nullam rutrum dui in placerat suscipit. Aliquam a dapibus purus. Nulla enim ante, cursus non urna vel, egestas ullamcorper felis. Nullam laoreet orci turpis, vitae efficitur lacus pulvinar sagittis. Nam justo ipsum, rutrum non accumsan sed, molestie eu purus. Curabitur imperdiet nisl sed mi varius, in accumsan purus dignissim. Phasellus consequat sollicitudin massa, et rutrum arcu feugiat ut. Pellentesque lacus arcu, volutpat nec nisi vel, commodo finibus orci.</p>

      <p>Nulla cursus sem id dolor sagittis, sit amet hendrerit risus tristique. Nunc mattis condimentum enim, ut commodo mi sodales aliquam. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum nibh mi, pellentesque eget lacus in, condimentum condimentum nibh. Sed non porta augue. Etiam dictum ullamcorper sem at tristique. Curabitur ullamcorper nunc sed laoreet elementum. Vivamus volutpat consectetur nibh at dictum. Curabitur dictum est non ultrices varius. Aliquam a orci cursus, vestibulum augue ac, luctus ante. Praesent lobortis nibh in tellus accumsan, vitae pretium neque sollicitudin.</p>
    </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Project1",
  components: {},
  props: [],
  data() {
    return {
      projectOpen: null,
    };
  },
  methods: {
    projectToggle(clicked) {
if(clicked == this.projectOpen){
  this.projectOpen = null;
}
else{
      this.projectOpen = clicked;
}
    }
  }
};
</script>

<style lang="scss" scoped>
.project{
  position:relative;
}
.project1 {
  -webkit-transition: all 1s; /* Safari */
  transition: all 1s;
  min-height: 100vh;
  position:static;
  &.open {
    -webkit-transition: all 1s; /* Safari */
  transition: all 1s;
  background: #fff;
  top:0px;
  .showcase{
    img{
    }
  }
  }

  .showcase{
    -webkit-transition: all 1s; /* Safari */
    transition: all 1s;
    overflow: hidden;
    height:100vh;
    cursor:pointer;
    &:hover, &.open{
      .circle{
           top:-2px;
      width:56px;
      height:56px;
      line-height:52px;
        .label{

        .arrow{
       top:38px;
        left:23px
        }
        .close{
          line-height: 58px;
        }
}
      }
    }
    &.open{
      img{
      height:100vh;
      display:block;
position:relative;
top:-200px;
      }
    }
    img {
      -webkit-transition: all 10s; /* Safari */
      transition: all 10s;
      height: 100vh;
      width:auto;
      display: inline;
      text-align: center;
    }
    .circle{
    height:52px;
    width:52px;
    border-radius: 50%;
    background:#E5855E;
    position:relative;
    line-height: 49px;
    margin:0 auto;
    border:0px solid #fff;
    .label{
      vertical-align: middle;
      text-align: center;
      position:relative;
      .arrow{
        height:0px;
        width:0px;
        border-top:5px solid white;
        border-bottom:5px solid transparent;
        border-right: 5px solid transparent;
        border-left: 5px solid transparent;
        position:absolute;
        top:36px;
        left:21px;
      }
      span{
        font-size:12px;
        font-weight:700;
      }
    }
    &:hover, &.open {
      .span{

      }
      .arrow{
        top:36px;
        left:24px

      }
    }
    }
    .frame {
      width: 220px;
      height: 50px;
      margin: 0 auto;
      margin-top: 0px;
      position: static;
      cursor: pointer;
      -ms-transform: scale(0.18, 0.18); /* IE 9 */
      -webkit-transform: scale(0.18, 0.18); /* Safari */
      transform: scale(0.18, 0.18);
      z-index: 1000;
      &:hover {
        -ms-transform: scale(0.2); /* IE 9 */
        -webkit-transform: scale(0.2); /* Safari */
        transform: scale(0.2);
        .label {
          transform: scale(1);
          -webkit-transform: scale(1);
        }
      }
      .hex-outer {
        width: 210px;
        height: 120px;
        border-top: 105px solid red;
        border-left: 60px solid transparent;
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
      .hex-inner {
        background: #e5855e;
        width: 200px;
        height: 115px;
        border-top: 100px solid #c5988e;
        border-left: 210px solid transparent;
        position: relative;
        left: 0px;
        top: 82px !important;
        border-radius: 0;
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
        transition: all 0.4s;
        -webkit-transition: all 0.4s;

        /* Icons */

        #nav-icon1,
        #nav-icon2,
        #nav-icon3,
        #nav-icon4 {
          width: 60px;
          height: 45px;
          position: relative;
          top: 30px;
          left: 10px;
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
          border-radius: 9px;
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
      }
    }
    &:hover {
      img {
        -ms-transform: scale(1.2); /* IE 9 */
        -webkit-transform: scale(1.2); /* Safari */
        transform: scale(1.2);
      }
    }
    &.open {
      height: 50vh;
    }
  }
  .showcase-content {
    padding: 0px;
    -webkit-transition: all 1s; /* Safari */
    transition: all 1s;
    opacity: 1;
    height: 0px;
    overflow: hidden;
    &.open {
      opacity: 1;
      height: auto;
    }
    .container{

    
    p{
      
    }
    }
  }
}

.project1 .description {
  position: absolute;
}

.project1 .showcase h2 {
  color: white;
  text-transform: uppercase;
  font-weight: 800;
  font-size: 20px;
  margin: 0px 0px 10px 0;
  text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.8);
  text-align: center;
}

.project1 .showcase h3 {
  color: white;
  text-transform: uppercase;
  font-weight: 700;
  font-size: 15px;
  margin: 0px 0px 10px 0px;
  text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.8);
  text-align: center;
}
</style>