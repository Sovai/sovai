<template>
  <footer class="uk-flex uk-flex-middle uk-flex-between">
    <div class="uk-text-small uk-text-uppercase uk-margin-left">
      all rights reserved ~ SOVAI KEAN @{{ new Date().getFullYear() }}
    </div>
    <div class="uk-text-right">
      <ColorModePicker />
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 35px;
  right: 15px;
  .uk-text-small {
    font-size: 10px;
    color: rgba($color: var(--text-primary), $alpha: 0.1);
  }
}
</style>
