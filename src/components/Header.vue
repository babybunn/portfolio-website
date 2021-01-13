<template>
  <header id="header">
    <b-container>
      <b-row>
        <b-col cols="6">
          <nav class="nav nav-left">
            <router-link :to="{ hash: '#work'}">Work</router-link>
            <router-link :to="{ hash: '#about'}">About</router-link>
            <router-link :to="{ hash: '#exp'}">Experience</router-link>
          </nav>
        </b-col>
        <b-col cols="6">
          <nav class="nav nav-right justify-content-end">
            <router-link :to="{ hash: '#contact'}">Contact</router-link>
          </nav>
        </b-col>
      </b-row>
    </b-container>
    <div class="container">
      <div class="row">
      
        <div class="col-12 col">
          
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {

    }
  },
  mounted() {

  },
  methods: {
  }
}
</script>

<style scoped lang="scss">

</style>
