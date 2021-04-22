<template>
  <div class="home container-fluid bg-black">
    <div class="row text-right">
      <div class="col-6 pg-location">
        <h1 class="font-large font-jj col-location text-white">JONESY</h1>
        <br />
        <h1 class="font-large font-jj text-white">JAVA</h1>
      </div>
    </div>
    <div class="col-6">
      <div class="row">
        <div class="square one-bg one-location blocksRowOne"></div>
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

AOS.init()
export default {
  name: 'MyComponent',
  setup() {
    onMounted(() => {
      // called by CLASS in Div 'fancy'
      anime({
        targets: '.blocksRowOne',
        translateX: 0,
        delay: anime.stagger(100, { start: 100 })
      })
      anime({
        targets: '.blocksRowTwo',
        translateX: 150,
        delay: anime.stagger(200, { start: 100 })
      })
      anime({
        targets: '.blocksRowThree',
        translateX: 300,
        delay: anime.stagger(200, { start: 100 })
      })
      anime({
        targets: '.blocksRowFour',
        translateX: 450,
        delay: anime.stagger(200, { start: 100 })
      })
    })
    return {

    }
  }
}
</script>

<style scoped lang="scss">
.bg-black {
  background-color: #000000;
}
.font-large {
  font-size: 300px;
}
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
