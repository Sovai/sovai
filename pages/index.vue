<template>
  <div>
    <div class="uk-text-center">
      <h1 class="uk-h1 uk-margin-remove name">Sovai (Vc3nt) Kean</h1>
      <div class="uk-margin-small">
        <i>front-end</i> · <i>api</i> ·
        <i>salesforce</i>
      </div>

      <div class="uk-flex uk-flex-center icons uk-margin-small-top">
        <span
          class="uk-padding-small uk-padding-remove-vertical"
          uk-icon="icon: github-alt"
        />
        <span
          class="uk-padding-small uk-padding-remove-vertical"
          uk-icon="icon: linkedin"
        />
        <span
          class="uk-padding-small uk-padding-remove-vertical"
          uk-icon="icon: reddit"
        />
        <span
          class="uk-padding-small uk-padding-remove-vertical"
          uk-icon="icon: facebook"
        />
        <span uk-icon="icon: instagram" />
      </div>

      <hr class="hr" />
      <div class="uk-text-left uk-margin-top">
        <div class="uk-text-lead">
          សួស្តី!
        </div>
      </div>
    </div>
    <splash />
  </div>
</template>

<script>
import Splash from '~/components/Splash'
export default {
  components: { Splash },
}
</script>

<style scoped lang="scss">
@import '~/assets/scss/variables';
.name {
  font-family: 'Rajdhani';
}
.icons span:hover {
  color: $link-color;
  cursor: pointer;
}
</style>
