/* eslint-disable no-irregular-whitespace */
<template>
  <div class="testimonial" id="testimonial">
    <b-container fluid class="px-0">
      <b-row class="justify-content-end">
        <b-col>
          <h2 class="title-testimonial">
            <span><strong>What collegues are saying about me</strong></span>
            <span><strong>What collegues are saying about me</strong></span>
          </h2>
        </b-col>
      </b-row>
    </b-container>
    <b-container>
      <b-row class="mt-5">
        <b-col>
          <img
            src="@/assets/images/format-quote-open.svg"
            alt="quote-left-open"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col cols="12">
          <div class="testimonial-item">
            <div class="swiper-container">
              <!-- Additional required wrapper -->
              <div class="swiper-wrapper">
                <!-- Slides -->
                <div
                  class="swiper-slide"
                  v-for="(testimonial, index) in testimonials"
                  :key="index"
                >
                  <div class="row">
                    <div class="col-12 col-md-7 offset-md-1">
                      <div class="testimonial">
                        <div class="testimonial-body">
                          <p>
                            {{ testimonial.content }}
                          </p>
                        </div>
                        <div
                          class="testimonial-footer d-flex align-items-center"
                        >
                          <div class="testimonial-img mr-3">
                            <b-img
                              :src="testimonial.img"
                              :alt="testimonial.name"
                              rounded="circle"
                            ></b-img>
                          </div>
                          <div class="testimonial-info">
                            <h4>
                              <strong>{{ testimonial.name }}</strong>
                            </h4>
                            <p class="testimonial-title">
                              {{ testimonial.title }}
                            </p>
                            <p class="testimonial-company">
                              {{ testimonial.company }}
                            </p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- If we need navigation buttons -->
          <div class="swiper-button-next"></div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import Swiper, { Navigation, Pagination, Autoplay } from 'swiper'
import 'swiper/swiper-bundle.css'

Swiper.use([Navigation, Pagination, Autoplay])

export default {
  name: 'Testimonials',
  data() {
    return {
      testimonials: [
        {
          content:
            "Kudos for all projects she had work on. She has a sense of design and her skill on website development is great. She had never give up for any difficult situations and don't afraid for any change. Highly recommend this person!",
          name: 'Orawee Hinthong',
          title: 'Frontend Developer Manager, Production Director',
          company: 'Prontomarketing',
          img: require('@/assets/images/onn.png')
        },
        {
          content:
            "Pang is invaluable to Mezcal team. She eats complex problems for breakfast and always finds a way to solve the issue. Whenever we're desperate we go to Pang. Not sure how she does it.  She is the MacGyver of the team! Probably she is hiding this toolkit under her desk:",
          name: 'Martins Benkitis',
          title: 'Senior Project Manager',
          company: 'Prontomarketing',
          img: require('@/assets/images/martins.png')
        }
      ]
    }
  },
  mounted() {
    new Swiper('.swiper-container', {
      loop: true,
      effect: 'fade',
      autoplay: {
        delay: 3000
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
      }
    })
  }
}
</script>

<style scoped lang="scss">
.title-title-testimonial {
  padding-bottom: 10%;
}
.testimonial {
  overflow: hidden;
  padding-top: 100px;
}
.testimonial-body {
  margin-bottom: 40px;
  p {
    font-size: 30px;
    margin-bottom: 10px;
    @media (max-width: 991px) {
      font-size: 20px;
    }
  }
}
.testimonial-footer h4 {
  font-size: 26px;
  @media (max-width: 991px) {
      font-size: 18px;
    }
}
.testimonial-footer p {
  font-size: 16px;
  margin-bottom: 0;
  @media (max-width: 991px) {
      font-size: 14px;
    }
}
.swiper-button-next {
    background: transparent;
    width: 20%;
    height: 100%;
    top: 0;
    right: 0;
    &:after {
      display: none;
    }
}
</style>
