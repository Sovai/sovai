<template>
  <nav class="uk-navbar-container uk-navbar-transparent uk-margin" uk-navbar>
    <div class="uk-navbar-right">
      <ul class="uk-navbar-nav">
        <li v-if="$route.name !== 'index'">
          <nuxt-link to="/">home</nuxt-link>
        </li>

        <li>
          <nuxt-link to="/about">who?</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/maintenance">skills</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/maintenance">projects</nuxt-link>
        </li>
        <li>
          <nuxt-link to="https://it-tools.tech/git-memo">tools</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/maintenance">blog</nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style></style>
