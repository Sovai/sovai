<template>
  <div class="landing__vertical">
    <p class="landing__stat">
      all rights reserved ~ SOVAI KEAN @{{ new Date().getFullYear() }}
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.landing__vertical {
  position: absolute;
  display: flex;
  align-items: center;
  left: 3.75rem;
  bottom: 0;
  margin-top: 12rem;
  padding: 0.75rem 0;
  transform: rotate(-90deg);
  transform-origin: 0 50%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  transition: color 175ms cubic-bezier(0.4, 0.25, 0.3, 1);
  white-space: nowrap;
}
.landing__stat {
  display: flex;
  align-items: center;
  position: relative;
  text-transform: uppercase;
  font-size: 10px;
  color: rgba($color: var(--text-primary), $alpha: 0.1);
}
</style>
