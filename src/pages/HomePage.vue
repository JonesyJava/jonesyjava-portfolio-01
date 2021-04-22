<template>
  <div class="home container-fluid">
    <div class="row text-right">
      <div class="col-6 pg-location">
        <h1 class="font-large">JONESY</h1>
        <br />
        <h1 class="font-large">JAVA</h1>
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
        targets: '.fancy',
        translateX: 270,
        delay: anime.stagger(100)
      })
    })
    return {

    }
  }
}
</script>

<style scoped lang="scss">
.font-large {
  font-size: 150px;
}
.pg-location {
  position: absolute;
  top: 300px;
}
</style>
