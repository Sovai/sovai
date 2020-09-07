<template>
  <div class="wrap">
    <app-header />
    <Nuxt />
    <app-footer />
  </div>
</template>
<script>
import AppHeader from '~/components/AppHeader'
import AppFooter from '~/components/AppFooter'
export default {
  components: {
    AppHeader,
    AppFooter,
  },
}
</script>
<style lang="scss" scoped>
.wrap {
  width: 100vw;
  height: 100vh;
  max-height: 100vh;
  position: relative;
  overflow: hidden;
}
</style>
