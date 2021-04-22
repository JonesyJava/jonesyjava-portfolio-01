<template>
  <div class="home container-fluid bg-black">
    <div class="row text-right">
      <div
        class="col-6 pg-location"
        data-aos="fade-left"
        data-aos-offset="500"
        data-aos-duration="1000"
      >
        <h1 class="font-large font-jj col-location text-white">Mike</h1>
        <br />
        <h1 class="font-large font-jj text-white">Jones</h1>
      </div>
    </div>
    <div class="col-6">
      <div class="row">
        <div
          class="square one-bg one-location blocksRowOne hover-about text-center pt-4"
        >
          <h2 class="bio mt-3">BIO</h2>
        </div>
      </div>
      <div class="row">
        <div class="square one-bg two-location blocksRowOne"></div>
        <div class="square two-bg two-location blocksRowTwo"></div>
      </div>
      <div class="row">
        <div class="square one-bg four-location blocksRowOne"></div>
        <div class="square two-bg four-location blocksRowTwo"></div>
        <div class="square three-bg four-location blocksRowThree"></div>
      </div>
      <div class="row">
        <div class="square one-bg seven-location blocksRowOne"></div>
        <div class="square two-bg seven-location blocksRowTwo"></div>
        <div class="square three-bg seven-location blocksRowThree"></div>
        <div class="square four-bg seven-location blocksRowFour"></div>
      </div>
    </div>
  </div>
</template>

<script>
import { onMounted } from 'vue'
import anime from 'animejs/lib/anime.min.js'
import AOS from 'aos'
import 'aos/dist/aos.css'

AOS.init()
export default {
  name: 'MyComponent',
  setup() {
    onMounted(() => {
      // called by CLASS in Div 'fancy'
      anime({
        targets: '.blocksRowOne',
        translateX: 0,
        delay: anime.stagger(100, { start: 1000 })
      })
      anime({
        targets: '.blocksRowTwo',
        translateX: 150,
        delay: anime.stagger(500, { start: 1000 })
      })
      anime({
        targets: '.blocksRowThree',
        translateX: 300,
        delay: anime.stagger(500, { start: 1000 })
      })
      anime({
        targets: '.blocksRowFour',
        translateX: 450,
        delay: anime.stagger(1000, { start: 1000 })
      })
    })
    return {

    }
  }
}
</script>

<style scoped lang="scss">
// Hover within Blocks
.hover-about:hover {
  background-color: aliceblue;
  cursor: pointer;
}
.hover-about:hover .bio {
  display: inline-block;
}
.bio {
  display: none;
}
.hover-about {
  transition: all 0.25s;
}
// Background Color
.bg-black {
  background-color: #000000;
}

// Font Size
.font-large {
  font-size: 300px;
}

// Page Position
.pg-location {
  position: absolute;
  top: 150px;
}
.font-jj {
  font-family: "Bebas Neue" !important;
}
.col-location {
  position: relative;
  top: 94px;
}
.square {
  height: 125px;
  width: 135px;
}
.one-location {
  position: absolute;
  top: 17rem;
  right: -150px;
}
.two-location {
  position: absolute;
  top: 25rem;
  right: -150px;
}

.four-location {
  position: absolute;
  top: 33rem;
  right: -150px;
}
.seven-location {
  position: absolute;
  top: 41rem;
  right: -150px;
}
.one-bg {
  background-color: #006336;
}
.two-bg {
  background-color: #02854a;
}
.three-bg {
  background-color: #029653;
}
.four-bg {
  background-color: #01c76e;
}
</style>
