<script setup>

import { RouterLink } from 'vue-router';

defineProps({
  bg: {
    type: String,
    default: 'bg-gray-100'
  }, 
  title: {
    type: String,
    default: 'Please add title'
  },
  subtitle: {
    type: String,
    default: 'Please add subtitles'
  },
  buttonValue: {
    type: String,
    default: 'Submit'
  },
  href: {
    type: String,
    default: '/'
  },
  buttonBg: {
    type: String,
    default: 'bg-black'
  },
  hover: {
    type: String,
    default: 'bg-gray-700'
  }
})

</script>

<template>
  <div :class="`${bg} p-6 rounded-lg shadow-md`">
    <h2 class="text-2xl font-bold">{{title}}</h2>
      <p class="mt-2 mb-4">
        {{subtitle}}
      </p>
      <RouterLink
        :to="`${href}`"
        :class="`inline-block ${buttonBg} text-white rounded-lg px-4 py-2 hover:${hover}`"
      >
        {{buttonValue}}
      </RouterLink>
  </div>
</template>