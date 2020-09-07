<template>
  <div class="image uk-text-center">
    <h1 class="uk-h1 uk-margin-remove name">
      Sovai Kean
    </h1>
    <small>aka Vc3nt</small>

    <home-page />

    <div class="uk-margin-small">
      <i>front-end</i> · <i>api</i> ·
      <i>salesforce</i>
    </div>

    <div class="uk-flex uk-flex-center icons uk-margin-small-top">
      <span
        class="uk-padding-small uk-padding-remove-vertical"
        uk-icon="icon: github-alt"
        @click="external"
      />
      <span
        class="uk-padding-small uk-padding-remove-vertical"
        uk-icon="icon: linkedin"
        @click="external"
      />
      <span
        class="uk-padding-small uk-padding-remove-vertical"
        uk-icon="icon: facebook"
        @click="external"
      />
      <span uk-icon="icon: instagram" @click="external" />
    </div>
  </div>
</template>

<script>
export default {
  mounted() {},
  methods: {
    external(type) {
      this.$router.push('/maintenance')
    },
  },

  head: {
    title: 'Sovai Kean',
    meta: [
      {
        hid: 'sovai',
        name: 'description',
        content: 'Sovai kean @SISKH',
      },
      {
        proprty: 'og:url',
        content: 'Sovai Kean',
      },
      {
        proprty: 'og:type',
        content: 'home page',
      },
      {
        proprty: 'og:title',
        content: 'Sovai Kean',
      },
      {
        proprty: 'og:description',
        content: 'Sovai Kean',
      },
      {
        proprty: 'og:image',
        content: require('image/sovai.jpg'),
      },
    ],
    noscript: [{ innerHTML: 'Body No Scripts', body: true }],
  },
}
</script>

<style scoped lang="scss">
@import '~/assets/scss/variables';

.image {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.name {
  font-family: 'Rajdhani';
}
.icons span:hover {
  color: $link-color;
  cursor: pointer;
}
</style>
