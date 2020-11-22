<template>
  <header class="bg-indigo-900 relative py-32">
    <span class="absolute inset-0 h-full w-full bg-black bg-opacity-50 z-0"></span>
    <div class="container z-10 relative mx-auto xl:w-1/2">
      <h1 class="uppercase text-white text-4xl font-bold">
        Kecharrm
      </h1>
      <p class="text-white text-opacity-90 w-1/3 my-2 mb-8">
        Kecharrm is a multi-domain community built after a server gathering.
      </p>
      <div class="container flex flex-row space-x-2">
        <Button type="dark">
          Découvrir
        </Button>
        <button class="text-white py-1 px-4 focus:outline-none">
          Rejoindre le discord
        </button>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'
import Button from '~/components/button.vue'

export default Vue.extend({
  components: {
    Button,
  },  
})
</script>