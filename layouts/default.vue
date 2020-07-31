<template>
  <div class="uk-container uk-margin-top">
    <div class="uk-grid uk-flex uk-flex-center" uk-grid>
      <div class="uk-width-2-3">
        <app-header />
        <Nuxt />
      </div>
    </div>
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
