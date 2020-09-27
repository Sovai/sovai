<template>
  <div class="image uk-text-center">
    <h1 class="uk-h1 uk-margin-remove name">
      <span>S</span>ovai <span>K</span>ean
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
    title: 'Sovai Kean - Portfolio',
    meta: [
      {
        name: 'title',
        content: 'Sovai Kean - Portfolio',
      },
      {
        hid: 'sovai',
        name: 'description',
        content:
          'Welcome to sovai.dev, my official portfolio. You can find my CV, projects, and all my blog posts.',
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
        content: '/image/sovai.jpg',
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
  text-transform: uppercase;
  font-size: 27px;
  font-family: 'Rajdhani';
  span {
    font-size: 37px;
  }
}
.icons span:hover {
  color: var(--color-primary);
  cursor: pointer;
}
</style>
