<template>
  <div>
    <component
      :is="`icon-${colors[index]}`"
      :class="getClasses(colors[index])"
      @click="
        index === colors.length - 1 ? (index = 0) : index++
        $colorMode.preference = colors[index]
      "
    />
    <!-- <ul>
      <li v-for="color of colors" :key="color">
        <component
          :is="`icon-${color}`"
          :class="getClasses(color)"
          @click="$colorMode.preference = color"
        />
      </li>
    </ul> -->
    <!-- <p>
      <ColorScheme placeholder="..." tag="span">
        Color mode: <b>{{ $colorMode.preference }}</b>
        <span v-if="$colorMode.preference === 'system'"
          >(<i>{{ $colorMode.value }}</i> mode detected)</span
        >
      </ColorScheme>
    </p> -->
  </div>
</template>

<script>
// import IconSystem from '@/assets/icons/system.svg?inline'
import IconLight from '@/assets/icons/light.svg?inline'
import IconDark from '@/assets/icons/dark.svg?inline'
import IconSepia from '@/assets/icons/sepia.svg?inline'
export default {
  components: {
    // IconSystem,
    IconLight,
    IconDark,
    IconSepia,
  },
  data() {
    return {
      index: 0,
      colors: ['dark', 'light', 'sepia'],
    }
  },
  methods: {
    getClasses(color) {
      // Does not set classes on ssr preference is system (because we know them on client-side)
      if (this.$colorMode.unknown) {
        return {}
      }
      return {
        preferred: color === this.$colorMode.preference,
        selected: color === this.$colorMode.value,
      }
    },
  },
}
</script>

<style scoped>
.feather {
  position: relative;
  top: 0px;
  cursor: pointer;
  margin: 0;
  border-radius: 5px;
  transition: all 0.1s ease;
}
.feather:hover {
  top: -3px;
}
.feather.preferred {
  border-color: var(--color-secondary);
  top: -3px;
}
.feather.selected {
  color: var(--color-secondary);
}
</style>
