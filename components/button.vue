<template>
  <div>
    <button v-if="type === 'dark' && !outline" class="bg-white text-indigo-800 font-medium hover:bg-indigo-50 hover:text-indigo-900 py-1 px-2 border border-transparent">
      <slot />
    </button>
    <button v-else-if="type === 'light' && !outline" class="bg-indigo-800 text-white font-medium py-1 px-2 hover:bg-indigo-900 border border-transparent">
      <slot />
    </button>
    <button v-else-if="type === 'light' && outline" class="text-indigo-800 py-1 px-2 border border-indigo-800">
      <slot />
    </button>
    <button v-else class="text-white py-1 px-2 border border-white">
      <slot />
    </button>
  </div>
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
    outline : {
      type: Boolean,
      required: false,
      default: false,
    } as PropOptions<Boolean>,
  },
  methods: {
    isDark(): Boolean {
      return this.type === 'dark';
    }
  },
})
</script>