<template>
  <button
    :class="{'bg-white text-indigo-800 font-medium hover:bg-indigo-50 hover:text-indigo-900': isDark(), 'bg-indigo-800 text-white font-medium hover:bg-indigo-900': !isDark()}"
    class="py-1 px-4 transition-colors duration-200"
  >
    <slot />
  </button>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'

type Buttons = 'dark' | 'light';

export default Vue.extend({
  props: {
    type: {
      type: String,
      required: true,
    } as PropOptions<Buttons>,
  },
  methods: {
    isDark(): Boolean {
      return this.type === 'dark';
    }
  },
})
</script>