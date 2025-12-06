<template>
  <section>
    <div class="container">
      <h1 class="display-3 section-title color">Me, Myself & I</h1>
      <div class="row g-5 mt-1">
        <div class="col-lg-5 left-side">
          <p class="about-text">
            I'm an Egyptian
            <span class="keyword">knowledge seeker</span>. I have an enthusiatic
            passion for <span class="keyword">CS & IT</span>, which I found at
            the age of 13. So far, I've been self-studying to grow this passion
            (and hosting hackathons with the
            <a href="https://the.hackfoundation.org">Hack Foundation</a> help
            high schoolers do the same). I have also been mesmerized by
            Astrophysics/Astornomy and have done a few
            <a
              href="https://github.com/Geo-sudo/Projects/tree/main/Computational-Astrophysics"
            >
              computational projects</a
            >
            and co-authored a
            <a
              href="https://www.researchgate.net/publication/398367184_A_comparison_galactic_formation_evolution_through_semi-analytic_and_numerical_hydrodynamic_frameworks_in_the_context_of_extragalactic_astronomy"
            >
              review article</a
            >. I'm also a Christian Oriental Orthodox!
          </p>
          <img class="spider-web" src="../assets/coptic.png" alt="" />
        </div>
        <div class="col-lg-7">
          <transition name="fade-quote" mode="out-in">
            <div
              class="quote-container"
              v-if="quoteNumber != null"
              @click="resetAndChangeQuote()"
            >
              <div class="quote-img">
                <img :src="quotes[quoteNumber]['quote-img']" />
              </div>
              <p class="quote">{{ quotes[quoteNumber]["quote"] }}</p>
              <p class="quote-cite">{{ quotes[quoteNumber]["quote-cite"] }}</p>
            </div>
          </transition>
        </div>
      </div>
    </div>
    <div class="d-none" id="imgs-preloader">
      <div class="d-none" v-for="img in quotes" :key="img">
        <img :src="img['quote-img']" />
      </div>
    </div>
  </section>
</template>
<script>
import nietzsche from "../assets/nietzsche.png";
import dumbledore from "../assets/dumbledore.png";
import augustine from "../assets/augustine.jpg";
import chaplin from "../assets/chaplin.png";
import frankl from "../assets/frankl.jpg";
import john from "../assets/john.png";
import sagan from "../assets/sagan.png";
import tertullian from "../assets/tertullian.png";

export default {
  name: "AboutView",
  props: ["themeColor"],
  data() {
    return {
      quoteNumber: null,
      changeQuote: null,
      lastone: null,
      shownQuotes: [],
      quotes: [
        {
          "quote-img": nietzsche,
          quote:
            '"There will always be rocks in the road ahead of us. They will be stumbling blocks or stepping stones; it all depends on how you use them."',
          "quote-cite": "- Friedrich Nietzsche",
        },
        {
          "quote-img": dumbledore,
          quote:
            '"It does not do to dwell on dreams and forget to live, remember that."',
          "quote-cite": "- Albus Dumbledore",
        },
        {
          "quote-img": augustine,
          quote:
            '"In doing what we ought we deserve no praise, because it is our duty."',
          "quote-cite": "- St. Augustine of Hippo",
        },
        {
          "quote-img": frankl,
          quote:
            '"When man can\'t find meaning in his life, he distracts himself with pleasure."',
          "quote-cite": "- Viktor E. Frankl",
        },
        {
          "quote-img": sagan,
          quote: '"Every one of us is, in the cosmic perspective, precious."',
          "quote-cite": "- Carl Sagan",
        },
        {
          "quote-img": chaplin,
          quote:
            '"Life is a tragedy when seen in close-up, but a comedy in long-shot."',
          "quote-cite": "- Charlie Chaplin",
        },
        {
          "quote-img": tertullian,
          quote:
            '"Truth persuades by teaching, but does not teach by persuading."',
          "quote-cite": "- Tertullian",
        },
        {
          "quote-img": john,
          quote:
            '"Evil is nothing else than absence of goodness, just as darkness also is absence of light. For goodness is the light of the mind, and, similarly, evil is the darkness of the mind."',
          "quote-cite": "- John of Damascus",
        },
      ],
    };
  },
  methods: {
    resetAndChangeQuote() {
      this.changeQuoteMethod();
      clearInterval(this.changeQuote);
      this.changeQuote = setInterval(() => {
        this.changeQuoteMethod();
      }, 10000);
    },
    changeQuoteMethod() {
      this.shownQuotes.push(this.quoteNumber);
      this.lastone = this.quoteNumber;
      this.quoteNumber = null;
      setTimeout(() => {
        if (this.shownQuotes.length == this.quotes.length) {
          this.shownQuotes = [this.lastone];
        }
        do {
          this.quoteNumber = Math.floor(Math.random() * this.quotes.length);
        } while (this.shownQuotes.includes(this.quoteNumber));
      }, 400);
    },
  },
  mounted() {
    // this.quoteNumber = Math.floor(Math.random() * this.quotes.length);
    this.quoteNumber = this.quotes.length - 1;
    // ThemeColor
    Array.from(document.getElementsByClassName("color")).forEach((element) => {
      element.classList.add(this.themeColor);
    });
    // End ThemeColor
    this.changeQuote = setInterval(() => {
      this.shownQuotes.push(this.quoteNumber);
      this.lastone = this.quoteNumber;
      this.quoteNumber = null;
      setTimeout(() => {
        if (this.shownQuotes.length == this.quotes.length) {
          this.shownQuotes = [this.lastone];
        }
        do {
          this.quoteNumber = Math.floor(Math.random() * this.quotes.length);
        } while (this.shownQuotes.includes(this.quoteNumber));
      }, 400);
    }, 10000);
  },
  unmounted() {
    clearInterval(this.changeQuote);
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";
@import url("https://fonts.googleapis.com/css2?family=Bree+Serif&display=swap");

.left-side {
  position: relative;
  z-index: 1;
  height: fit-content;
  .about-text {
    position: relative;
    padding-top: 1.5rem;
    padding-left: 1rem;
    letter-spacing: 0.4px;
    line-height: 1.7;
    font-size: 1.05rem;
    z-index: 1;
    .keyword {
      font-weight: 900;
      font-style: italic;
    }
    .DCollege {
      position: relative;
      &:hover {
        text-decoration: line-through;
      }
      &:hover::after {
        content: "Davidson College";
        height: fit-content;
        width: fit-content;
        min-width: 100%;
        white-space: pre;
        // background-color: red;
        position: absolute;
        bottom: -110%;
        left: 0;
        padding-top: 2px;
        text-align: center;
        color: rgb(214, 214, 214);
        font-weight: 900;
        font-size: 0.85em;
        font-style: italic;
      }
    }
    & ~ .spider-web {
      position: absolute;
      bottom: -35%;
      left: -20%;
      width: 30%;
      z-index: 0;
      path {
        fill: #555 !important;
      }
    }
  }
}

.quote-container {
  margin-top: -4.5rem;
  position: relative;
  .quote-img {
    position: relative;
    padding: 30px;
    padding-bottom: 4rem;
    &::after {
      content: "";
      position: absolute;
      display: block;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border-collapse: separate;
      box-shadow: inset 0 -15px 40px 80px $main-bg-color;
    }
    img {
      width: 100%;
      display: block;
    }
    // & ~ p {
    //   text-align: center;
    //   margin-top: -5rem;
    //   z-index: 2;
    // }
  }
  .quote {
    text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6), 0 0 6px rgba(0, 0, 0, 0.5);
    text-align: center;
    color: white;
    position: absolute;
    width: 70%;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    font-style: italic;
    font-family: "Bree Serif", serif;
    letter-spacing: 0.75px;
    font-size: 1.1rem;
  }
  .quote-cite {
    text-align: center;
    color: rgba(255, 255, 255, 0.7);
    position: absolute;
    bottom: -20px;
    right: 40px;
    font-style: italic;
    font-family: "Bree Serif", serif;
    letter-spacing: 0.75px;
    font-size: 0.95rem;
  }
}

@media (max-width: 991.98px) {
  .left-side {
    margin-top: 0.7rem;
    .spider-web {
      bottom: -15% !important;
      left: -12.5% !important;
    }
  }
  .quote-container {
    z-index: 1;
    margin-top: 0;
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    .quote-img {
      padding: 0;
      &::after {
        display: none;
      }
    }
    .quote {
      // bottom: -10px;
      position: relative;
      padding-top: 2rem;
      width: 90%;
    }
    .quote-cite {
      bottom: -40px;
      // position: relative;
    }
  }
}

.fade-quote-enter-active,
.fade-quote-leave-active {
  transition: all 0.4s ease;
}

.fade-quote-enter-from,
.fade-quote-leave-to {
  opacity: 0;
}

.fade-quote-enter-to,
.fade-quote-leave-from {
  opacity: 1;
}
</style>
