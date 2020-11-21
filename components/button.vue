<template>
  <button
    :class="{'bg-white text-indigo-800 font-medium': isDark()}"
    class="py-1 px-4"
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