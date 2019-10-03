<template>
  <div
  class="uk-background-norepeat uk-background-bottom-left uk-section uk-section-xlarge"
  :style="{ backgroundImage: 'url(' + require(`@/assets/${bg.cover}`) + ')' }"
  >
    <div class="uk-container">
      <div class="uk-grid-large uk-margin-large uk-grid">
        <div class="uk-grid-item-match uk-flex-middle uk-width-expand@m uk-first-column">
          <div class="uk-panel uk-width-1-1">
            <h2 class="uk-h1 uk-margin-small uk-text-left@m uk-text-center uk-scrollspy-inview uk-animation-slide-left-medium" uk-scrollspy-class="uk-animation-slide-left-medium">
            CIT Department
            </h2>
            <div class="uk-text-large uk-text-primary uk-margin-small uk-text-left@m uk-text-center uk-scrollspy-inview uk-animation-slide-top-medium">
              United States, New York, Morrisville
            </div>
            <div class="uk-margin-medium uk-text-left@m uk-text-center uk-scrollspy-inview uk-animation-slide-left-medium" uk-scrollspy-class="uk-animation-slide-left-medium">
              Here lies the students of CITA 430</br>
              Their dreams, ambitions, and future goals.</br>
              </br>
              Nothing is possible
            </div>
          </div>
        </div>
        <div class="uk-grid-item-match uk-flex-middle uk-width-expand@m">
          <div class="uk-panel uk-width-1-1">
            <div
            uk-slideshow="minHeight: 410; autoplay: true"
            class="uk-margin uk-slideshow uk-scrollspy-inview uk-animation-slide-top-medium"
            >
              <div class="uk-position-relative">
              <ul
              class="uk-slideshow-items"
              :style="{ minHeight: minHeight + 'px' }"
              >
                <li
                v-for="image in sliderImages"
                :key="image.src"
                active-class="uk-active uk-transition-active"
                tabindex="-1"
                >
                  <img
                  :src="require(`@/assets/${image.src}`)"
                  class="uk-cover"
                  alt=""
                  >
                  <div class="uk-overlay uk-overlay-primary uk-position-bottom uk-text-center uk-transition-slide-bottom">
                <h3 class="uk-margin-remove">CITA 430 Kids</h3>
              </div>
                </li>

              </ul>

                  <div class="uk-light">
                    <a
                    class="uk-position-medium uk-position-center-left uk-slidenav-previous uk-slidenav"
                    uk-slidenav-previous
                    uk-slideshow-item="previous"
                    >
                    </a>
                    <a
                    class="uk-position-medium uk-position-center-right uk-slidenav-next uk-slidenav"
                    uk-slidenav-next
                    uk-slideshow-item="next"
                    >
                    </a>
                  </div>

                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data: () => ({
    minHeight: 410,
    sliderImages: [
      {src: '6.png'},
      {src: '7.png'},
      {src: '2.jpg'},
      {src: '9.png'},
      {src: '10.png'},
      {src: '11.png'}
    ],
    bg: {
      cover: 'moville.png'
    }
  })
}
</script>
