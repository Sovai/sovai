<template>
  <div class="wrap">
    <app-header />
    <Nuxt />
  </div>
</template>
<script>
import AppHeader from '~/components/AppHeader'
export default {
  components: {
    AppHeader,
  },
}
</script>
<style lang="scss" scoped>
.wrap {
  width: 100vw;
  height: 100vh;
  position: relative;
  overflow: hidden;
}
</style>
