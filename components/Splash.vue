<template>
  <div>
    <h1 class="splash">
      <span class="text-wrapper">
        <span class="letters">hello, welcome!</span>
        <span class="line"></span>
      </span>
    </h1>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$anime
      .timeline({ loop: false })
      .add({
        targets: '.splash .line',
        scaleX: [0, 1],
        opacity: [0.5, 1],
        easing: 'easeInOutExpo',
        duration: 900,
      })
      .add({
        targets: '.splash .letter',
        opacity: [0, 1],
        translateX: [40, 0],
        translateZ: 0,
        scaleX: [0.3, 1],
        easing: 'easeOutExpo',
        duration: 800,
        offset: '-=600',
        delay: (el, i) => 150 + 25 * i,
      })
      .add({
        targets: '.splash',
        opacity: 0,
        duration: 1000,
        easing: 'easeOutExpo',
        delay: 1000,
      })
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.splash {
  font-weight: 200;
  font-size: 3.2em;
  background: $base-color;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

.splash .text-wrapper {
  display: inline-block;
  padding-top: 0.1em;
  padding-right: 0.05em;
  padding-bottom: 0.15em;

  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.splash .line {
  opacity: 0;
  position: absolute;
  left: 0;
  height: 2px;
  width: 100%;
  background-color: #fff;
  transform-origin: 100% 100%;
  bottom: 0;
}

.splash .letter {
  display: inline-block;
  line-height: 1em;
}
</style>
