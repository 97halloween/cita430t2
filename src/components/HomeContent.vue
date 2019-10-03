<template>
  <div
  class="uk-background-norepeat uk-background-bottom-left uk-section uk-section-xlarge"
  :style="{ backgroundImage: 'url(' + require(`@/assets/${bg.cover}`) + ')' }"
  >
    <div class="uk-container">
      <div class="uk-grid-large uk-grid-margin-large uk-grid">
        <div class="uk-width-expand@m uk-first-column">
          <h2 class="uk-h1 uk-width-xlarge uk-scrollspy-inview uk-animation-fade">
            Welcome to <br class="uk-visible@s"> CITA 430 project by <strong class="uk-heading-divider" id="strong">Team #2</strong>
          </h2>
        </div>

        <div class="uk-width-expand@m">
          <div class="uk-text-lead uk-margin-medium uk-scrollspy-inview uk-animation-fade">
            Let your dreams be your dreams.</br>
            Nothing is possible.</br>
            Just don't do it.
          </div>
          <div class="uk-margin uk-scrollspy-inview uk-animation-fade" uk-scrollspy-class="uk-animation-fade" style="">
            <img class="el-image uk-text-emphasis" :src="require(`@/assets/${image.sign}`)" width="112" height="21">
          </div>
        </div>
      </div>
    </div>

    <div class="uk-section uk-section-default">

    <video :src="require(`@/assets/video.mp4`)" class="uk-align-center" loop playsinline uk-video></video>

  </div>
  </div>
</template>

<script>
  export default {
    data: () => ({
      image: {
        sign: 'sign2.png'
      },
      bg: {
        cover: 'moville.png'
      }
    })
  }
</script>

<style scoped>
.uk-h1 {
  line-height: 1.2;
  font-family: Lato;
  text-transform: uppercase;
  letter-spacing: 3px;
}
.uk-text-lead {
  font-size: 18px;
  line-height: 1.625;
  font-family: Roboto Mono;
  font-weight: 100;
  text-transform: none;
  letter-spacing: -.2px;
}
</style>
