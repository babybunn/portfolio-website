<template>
  <div class="hero">
    <b-container>
      <b-row>
        <b-col>
          <h1 class="text-slide-animation" v-inview:class="['is-in-view']">
            <strong
              ><span class="text-line-wrapper"
                ><span class="text-line" style="transition-delay: 0ms;"
                  >Hello, I’m</span
                ></span
              ><br /><span class="text-secondary text-line-wrapper"
                ><span class="text-line" style="transition-delay: 100ms;"
                  >Wimonsiri Pokasame,</span
                ></span
              ><br /><span class="text-line-wrapper"
                ><span class="text-line" style="transition-delay: 200ms;"
                  >a Front-End Developer</span
                ></span
              ><br /><span class="text-line-wrapper"
                ><span class="text-line" style="transition-delay: 300ms;"
                  >based in Bangkok, Thailand.</span
                ></span
              ></strong
            >
          </h1>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  methods: {
  },
}
</script>

<style lang="scss" scoped></style>
