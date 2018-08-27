<template>
  <div class="home">
    <Hero/>
    <sui-button inverted primary size="massive">Make something</sui-button>
    <Sketches/>
  </div>
</template>

<script>
import Hero from "@/components/Hero.vue"
import Sketches from "@/components/Sketches.vue"

export default {
  name: 'home',
  components: {
    Hero,
    Sketches
  }
}
</script>

<style scoped>
.home {
  margin-bottom: 5px;
}
</style>