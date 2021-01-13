<template>
  <div class="experience" id="exp">
    <b-container>
      <b-row class="justify-content-end">
        <b-col sm="8">
          <h2 class="title-experience"><strong>Experience</strong></h2>
        </b-col>
      </b-row>
    </b-container>
    <b-container>
      <b-row class="justify-content-end">
        <b-col md="7">
          <div class="exp-item">
            <p class="exp-year text-secondary mb-2">Present</p>
            <h3 class="exp-company"><strong>Prontomarketing</strong></h3>
            <p class="exp-title">Frontend Developer</p>
          </div>
        </b-col>
      </b-row>
      <b-row class="justify-content-end">
        <b-col md="7">
          <div class="exp-item">
            <p class="exp-year text-secondary mb-2">2020</p>
            <h3 class="exp-company"><strong>SE Digital</strong></h3>
            <p class="exp-title">Senior Frontend Developer</p>
          </div>
        </b-col>
      </b-row>
      <b-row class="justify-content-end">
        <b-col md="7">
          <div class="exp-item">
            <p class="exp-year text-secondary mb-2">2019</p>
            <h3 class="exp-company"><strong>Ahancer</strong></h3>
            <p class="exp-title">Frontend Designer</p>
          </div>
        </b-col>
      </b-row>
      <b-row class="justify-content-end">
        <b-col md="7">
          <div class="exp-item">
            <p class="exp-year text-secondary mb-2">2016</p>
            <h3 class="exp-company"><strong>Prontomarketing</strong></h3>
            <p class="exp-title">Intern and Full-time Frontend Developer</p>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
.title-experience {
  padding-bottom: 10%;
}
.exp-year {
  font-size: 20px;
  font-weight: 600;
}
.exp-company {
  font-size: 40px;
}
.exp-title {
  font-size: 24px;
}
.exp-item {
  margin-bottom: 40px;
}
</style>
