<template>
  <div id="hero" :style="`background-image: url(${bgSrc});`"></div>
</template>


<script>
export default {
  name: 'HeroSection',
  props: ['bgSrc']
}
</script>


<style lang="scss" scoped>

#hero {
  background-size: cover;
  height: 320px;
}
</style>