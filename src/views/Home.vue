<template>
  <div class="home">
    <!-- <div class="cursor">
      <div class="cursor__ball cursor__ball--big ">
        <svg height="30" width="30">
          <circle cx="15" cy="15" r="12" stroke-width="0"></circle>
        </svg>
      </div>
      
      <div class="cursor__ball cursor__ball--small">
        <svg height="10" width="10">
          <circle cx="5" cy="5" r="4" stroke-width="0"></circle>
        </svg>
      </div>
    </div> -->
    <div class="cursor">
      <div class="cursor-slider" v-if="display">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="#fff" class="bi bi-arrow-right" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"/>
        </svg>
      </div>
    </div>

    <Header />
    <hero></hero>
    <work></work>
    <about></about>
    <experience></experience>
    <testimonials></testimonials>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Hero from '@/components/Hero.vue'
import About from '@/components/About.vue'
import Work from '@/components/Work.vue'
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'
import Experience from '@/components/Experience.vue'
import Testimonials from '@/components/Testimonials.vue'

import { gsap, CSSPlugin } from 'gsap/all'
gsap.registerPlugin(CSSPlugin)
import { TweenMax } from 'gsap'
import * as ScrollMagic from 'scrollmagic'
import { ScrollMagicPluginGsap } from 'scrollmagic-plugin-gsap'
gsap.registerPlugin(ScrollMagicPluginGsap)
ScrollMagicPluginGsap(ScrollMagic, gsap, TweenMax)

export default {
  name: 'Home',
  data() {
    return {
      display: false
    } 
  },
  components: {
    Hero,
    About,
    Work,
    Footer,
    Header,
    Experience,
    Testimonials
  },
  methods: {
    onMouseMove(e) {
      const cursor = document.querySelector('.cursor');

      TweenMax.to(cursor, 0.4, {
        x: e.pageX,
        y: e.pageY
      })
    },
    onMouseHover() {
      const bigBall = document.querySelector('.cursor');
      TweenMax.to(bigBall, 0.3, {
        scale: 4
      })
    },
    onMouseHoverOut() {
      const bigBall = document.querySelector('.cursor');
      TweenMax.to(bigBall, 0.3, {
        scale: 1
      })
    },
    onMouseHoverSlider() {
      const bigBall = document.querySelector('.cursor');
      TweenMax.to(bigBall, 0.3, {
        scale: 4
      });
      this.display = true;
    },
    onMouseHoverOutSlider() {
      const bigBall = document.querySelector('.cursor');
      TweenMax.to(bigBall, 0.3, {
        scale: 1
      });
      this.display = false;
    }

  },
  mounted() {
    const hoverables = document.querySelectorAll('.nav a');

    document.body.addEventListener('mousemove', this.onMouseMove);
    for (let i = 0; i < hoverables.length; i++) {
      hoverables[i].addEventListener('mouseenter', this.onMouseHover);
      hoverables[i].addEventListener('mouseleave', this.onMouseHoverOut);
    }

    const hoverSliderNav = document.querySelector('.swiper-button-next');
    hoverSliderNav.addEventListener('mouseenter', this.onMouseHoverSlider);
    hoverSliderNav.addEventListener('mouseleave', this.onMouseHoverOutSlider);

  }
}
</script>
