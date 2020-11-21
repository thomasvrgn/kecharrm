<template>
  <button>
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
  }
})
</script>