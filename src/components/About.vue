<template>
  <div id="about" class="about section" v-view>
    <div class="cover" v-view v-bind:class="{ 'sticky': stickyAbout, 'sticky-bottom': stickyAboutBottom  }" ref="coverAbout">
      <h1 class="align-center">About</h1>
      <Navbar/>
      <div class="middle-anchor" v-view="middleAnchorHandler"></div>
    </div>
    <div class="content" ref="contentAbout">
      <div class="story container">
        <h1>Organizational structure</h1>
<h2>Core investment banking activities</h2>
<p>Investment banking is split into front office, middle office, and back office activities. While large service investment banks offer all lines of business, both "sell side" and "buy side", smaller sell-side investment firms such as boutique investment banks and small broker-dealers focus on investment banking and sales/trading/research, respectively.
</p>
<p>Inns issuing securities and investors buying securities. For corporations, investment bankers offer information on when and how to place 
  their securities on the open market, an activity very important to an investment bank's reputation. Therefore, investment bankers play a very important role in 
  issuing new security offerings.[7]
</p>
<p>
<img src="http://lorempixel.com/600/300/" alt="">
</p>

<h3>Front office</h3>
<p>Front office is generally described as a revenue-generating role. There are two main areas within 
  front office: investment banking and markets[8]
  </p>
<p>Investment banking involves advising organizations on mergers and acquisitions, as well as a wide array of capital raising strategies.
Markets is divided into "sales and trading" (including "structuring"), and "research".
</p>
<h3>Corporate finance</h3>
<p>Corporate finance is the aspect of investment banks, which involves helping customers raise funds in capital markets and giving advice on mergers and acquisitions (M&A); this may involve subscribing investors to a security issuance, coordinating with bidders, or negotiating with a merger target. A pitch book of financial information is generated to market the bank to a potential M&A client; if the pitch is successful, the bank arranges the deal for the client. The investment banking division (IBD) is generally divided into industry coverage and product coverage groups. Industry coverage groups focus on a specific industry—such as healthcare, public finance (governments), FIG (financial institutions group), industrials, TMT (technology, media, and telecommunications), P&E (power & energy), consumer/retail, food & beverage, corporate defense and governance—and maintain relationships with corporations within the industry to bring in business for the bank. Product coverage groups focus on financial products—such as mergers and acquisitions, leveraged finance, public finance, asset finance and leasing, structured finance, restructuring, equity, debt issuance.
</p>
<p>
  <img src="http://lorempixel.com/600/300/" alt="">
</p>
<h3>Sales and trading</h3>
<p>On behalf of the bank and its clients, a large investment bank's primary function is buying and selling products.[9] In market making, traders will buy and sell financial products with the goal of making money on each trade. Sales is the term for the investment bank's sales force, whose primary job is to call on institutional and high-net-worth investors to suggest trading ideas (on a caveat emptor basis) and take orders. Sales desks then communicate their clients' orders to the appropriate trading rooms, which can price and execute trades, or structure new products that fit a specific need. Structuring has been a relatively recent activity as derivatives have come into play, with highly technical and numerate employees working on creating complex structured products which typically offer much greater margins and returns than underlying cash securities. In 2010, investment banks came under pressure as a result of selling complex derivatives contracts to local municipalities in Europe and the US.[10] Strategists advise external as well as internal clients on the strategies that can be adopted in various markets. Ranging from derivatives to specific industries, strategists place companies and industries in a quantitative framework with full consideration of the macroeconomic scene. This strategy often affects the way the firm will operate in the market, the direction it would like to take in terms of its proprietary and flow positions, the suggestions salespersons give to clients, as well as the way structurers create new products. Banks also undertake risk through proprietary trading, performed by a special set of traders who do not interface with clients and through "principal risk"—risk undertaken by a trader after he buys or sells a product to a client and does not hedge his total exposure. Banks seek to maximize profitability for a given amount of risk on their balance sheet. The necessity for numerical ability in sales and trading has created jobs for physics, computer science, mathematics and engineering Ph.D.s who act as quantitative analysts.
</p>
<h3>Research</h3>
<p>The securities research division reviews companies and writes reports about their prospects, often with "buy", "hold" or "sell" ratings. Investment banks typically have sell-side analysts which cover various industries. Their sponsored funds or proprietary trading offices will also have buy-side research. While the research division may or may not generate revenue (based on policies at different banks), its resources are used to assist traders in trading, the sales force in suggesting ideas to customers, and investment bankers by covering their clients.[citation needed] Research also serves outside clients with investment advice (such as institutional investors and high-net-worth individuals) in the hopes that these clients will execute suggested trade ideas through the sales and trading division of the bank, and thereby generate revenue for the firm. Research also covers credit research, fixed income research, macroeconomic research, and quantitative analysis, all of which are used internally and externally to advise clients but do not directly affect revenue. All research groups, nonetheless, provide a key service in terms of advisory and strategy. There is a potential conflict of interest between the investment bank and its analysis, in that published analysis can impact the performance of a security (in the secondary markets or an initial public offering) or influence the relationship between the banker and its corporate clients, thereby affecting the bank's profitability .[citation needed]
</p>
<h3>Middle office</h3>
<p>This area of the bank includes treasury management, internal controls (such as Risk), and internal corporate strategy.</p>

<p>Corporate treasury is responsible for an investment bank's funding, capital structure management, and liquidity risk monitoring.</p>

<p>Internal control tracks and analyzes the capital flows of the firm, the finance division is the principal adviser to senior management on essential areas such as controlling the firm's global risk exposure and the profitability and structure of the firm's various businesses via dedicated trading desk product control teams. In the United States and United Kingdom, a comptroller (or financial controller) is a senior position, often reporting to the chief financial officer.
</p>
      </div>
    </div>
    <div class="upper-anchor" v-view="upperAnchorHandler"></div>
    <div class="lower-anchor" v-view="lowerAnchorHandler"></div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "About",
  props: [],
  data() {
    return {
      stickyAbout: false,
      stickyAboutBottom: false,
      bounding: null
    };
  },
  components: {
    Navbar
  },
  methods: {
    //viewHandlerExamples(e) {
      //console.log(e.type) // 'enter', 'exit', 'progress'
      //console.log(e.percentInView) // 0..1 how much element overlap the viewport
      //console.log(e.percentTop) // 0..1 position of element at viewport 0 - above , 1 - below
      //console.log(e.percentCenter) // 0..1 position the center of element at viewport 0 - center at viewport top, 1 - center at viewport bottom
      //console.log(e.scrollPercent) // 0..1 current scroll position of page
      // console.log(e.scrollValue) // 0..1 last scroll value (change of page scroll offset)
      //console.log(e.target.rect) // element.getBoundingClientRect() result
      //console.log(this.stickyAbout)
    //},
    upperAnchorHandler(e) {
      //Scrolling up
      if (e.scrollValue < 0) {
        if (e.type === "enter") {
          this.stickyAbout = false;
          this.stickyAboutBottom = false;
          this.$router.push('#about')
        }
      }
      //Scrolling down
      if (e.scrollValue > 0 && e.scrollValue < 600) {
        if (e.type === "exit") {
          this.stickyAbout = true;
          this.stickyAboutBottom = false;
          this.$router.push('#about')
          // console.log(e)
        }
      }
    },
    middleAnchorHandler(e) {
      
      //Scrolling up
      //if (e.scrollValue < 0) {
      //   if (e.percentTop <= 0.5) {

      //   }
      // }
      // //Scrolling down
      // if (e.scrollValue > 0) {
      if (e.type === "progress") {
      //     this.$router.push('#about')
      if (e.percentTop <= 0.5) {
        this.stickyAbout = true;
      }
         }
      // }
    },

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
  },
  mounted() {}
};
</script>


<style lang="scss">
.about {
  position: relative;
  .cover {
    padding: 10px;
    height: 100vh;
    min-height: 100vh;
    background: #E5855E;
    position: relative;
    color:#fff;
    -webkit-transform:translate3d(0,0,0);
    transform:translate3d(0,0,0);
    -webkit-backface-visibility: hidden;
    top:0;
    bottom:auto;
    -webkit-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.25);
-moz-box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.25);
box-shadow: 1px 1px 5px 0px rgba(0,0,0,0.25);
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
    background:#fff;
    position: relative;
    .story{
    ul{margin:0px;}
    }
    .nav {
    position: absolute;
    bottom: 0px;
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
    bottom: 0;
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
  .about {
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
