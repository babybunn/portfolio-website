/* eslint-disable prettier/prettier */
<template>
  <div class="work py-5" >
    <b-container>
      <b-row class="align-items-center">
        <b-col xs="12">
          <h2 class="title text-center"><strong>Works</strong></h2>
        </b-col>
      </b-row>
      <b-row id="work">
        <b-col cols="12">
          <a class="work work-big pin work-primary" id="workVideo_1"  href="https://www.orchestratetech.com/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper">
              <div class="work-videoWrapper">
                <div class="wistia_embed wistia_async_j5sw99q6q1"></div>
              </div>
              <div class="work-txt">
                  <div class="work-txt-inner">
                    <h3>Orchestrate</h3>
                    <p>Wordpress Frontend Development</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
      </b-row>
    </b-container>
    <b-container fluid>
      <b-row class="align-items-center justify-content-center">
        <b-col xs="12" md="4" class="mt-5">
          <a class="work work-small work-secondary" href="https://www.prontodenim.com/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-prontoDenim mx-auto" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h4>Pronto Denim</h4>
                  <p>Wordpress & Theme development</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
        <b-col xs="12" md="5" class="mt-5"  offset-md="1">
          <a class="work work-medium work-secondary" href="https://www.wheelandanchor.ca/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-wheelanchor" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>Wheel & Anchor</h3>
                  <p>Wordpress & Theme development</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
      </b-row>

      <b-row class="align-items-center justify-content-center">
        <b-col xs="12" md="5" class="mt-5">
          <a class="work work-medium work-secondary" href="https://www.ipenwedding.com/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-ipen" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>iPen Wedding</h3>
                  <p>Wordpress Frontend Development</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
        <b-col xs="12" md="4" class="mt-5"  offset-md="1">
          <a class="work work-small work-secondary" href="https://www.boutiquebyhermosa.com/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-boutiquebyhermosa mx-auto" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>Boutique by Hermosa</h3>
                  <p>Wordpress E-Commerce Website</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
      </b-row>
    </b-container>
    <b-container>
      <b-row>
        <b-col cols="12">
          <a class="work work-big pin work-primary" id="workVideo_2"  href="https://se.digital/en" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper">
              <div class="work-videoWrapper">
                <div class="wistia_embed wistia_async_ulrdmcq0hg"></div>
              </div>
              <div class="work-txt">
                  <div class="work-txt-inner">
                    <h3>SE Digital</h3>
                    <p>Website Development (Vue.js)</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
      </b-row>
      </b-container>
      <b-container fluid>
        <b-row class="align-items-center justify-content-center">
        <b-col xs="12" md="4" class="mt-5">
          <div class="work work-small work-secondary">
            <div class="work-wrapper bg-ahancerfood mx-auto" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>FoodWalk</h3>
                  <p>UX/UI Design</p>
                  </div>
              </div>
            </div>
          </div>
        </b-col>
        <b-col xs="12" md="5" class="mt-5"  offset-md="1">
          <a class="work work-medium work-secondary" href="#" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-cce" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>Chonburi Clean Energy</h3>
                  <p>Wordpress & Theme Development</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col>
        <!-- <b-col xs="12" md="5" class="mt-5"  offset-md="1">
          <a class="work work-medium" href="https://www.wheelandanchor.ca/" target="_blank" rel="noreferrer noopener">
            <div class="work-wrapper bg-setoken" data-enllax-ratio="0.3">
              <div class="work-txt">
                <div class="work-txt-inner">
                  <h3>SE Digital</h3>
                  <h4>Token management platform</h4>
                  <p>UX/UI Design</p>
                  </div>
              </div>
            </div>
          </a>
        </b-col> -->
      </b-row>
    </b-container>
  </div>
</template>

<script>
import { gsap, CSSPlugin } from 'gsap/all'
gsap.registerPlugin(CSSPlugin)
import { TimelineMax, TweenMax, TimelineLite } from 'gsap'
import * as ScrollMagic from 'scrollmagic'
import { ScrollMagicPluginGsap } from 'scrollmagic-plugin-gsap'
gsap.registerPlugin(ScrollMagicPluginGsap)
ScrollMagicPluginGsap(ScrollMagic, TimelineMax, gsap, TweenMax, TimelineLite)

export default {
  name: 'Work',
  methods: {
    isInViewport(el) {
      var rect = el.getBoundingClientRect()
      return (
        rect.top >= 0 &&
        rect.left >= 0 &&
        rect.bottom <=
          (window.innerHeight || document.documentElement.clientHeight)
        //  && rect.right <= (window.innerWidth || document.documentElement.clientWidth) )
      )
    }
  },
  mounted() {
    const workBig = document.getElementsByClassName('work-big')[0]
    document.addEventListener(
      'scroll',
      function() {
        if (this.isInViewport(workBig)) {
          document
            .getElementsByClassName('work-big')[0]
            .classList.add('in-view')

          window._wq = window._wq || []
          window._wq.push({
            id: 'j5sw99q6q1',
            onReady: function(video) {
              video.play()
            }
          })
        } else {
          document
            .getElementsByClassName('work-big')[0]
            .classList.remove('in-view')
          window._wq = window._wq || []
          window._wq.push({
            id: 'j5sw99q6q1',
            onReady: function(video) {
              video.pause()
            }
          })
        }

        if (this.isInViewport(document.getElementById('workVideo_2'))) {
          document
            .getElementById('workVideo_2')
            .classList.add('in-view')

          window._wq = window._wq || []
          window._wq.push({
            id: 'ulrdmcq0hg',
            onReady: function(video) {
              video.bind('play', function() {
                video.time(3);
                return video.unbind;
              });
              video.play()
            }
          })
        } else {
          document
            .getElementById('workVideo_2')
            .classList.remove('in-view')
          window._wq = window._wq || []
          window._wq.push({
            id: 'ulrdmcq0hg',
            onReady: function(video) {
              video.pause()
            }
          })
        }

      }.bind(this),
      {
        passive: true
      } 
    )

    var controller = new ScrollMagic.Controller()

    new ScrollMagic.Scene({
      triggerElement: '#workVideo_1',
      triggerHook: 'onLeave',
      duration: '100%',
      offset: '-60'
    })
      .setPin('#workVideo_1')
      .addTo(controller)

      new ScrollMagic.Scene({
      triggerElement: '#workVideo_2',
      triggerHook: 'onLeave',
      duration: '100%',
      offset: '-60'
    })
      .setPin('#workVideo_2')
      .addTo(controller)
  }
}
</script>

<style scoped lang="scss">


</style>
