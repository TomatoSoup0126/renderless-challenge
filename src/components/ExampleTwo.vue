<script setup>
import { defineProps, defineEmits } from 'vue'
const props = defineProps({
  distance: {
    type: Number,
    required: true,
  },
  unit: {
    type: String,
    required: true,
  },
})
const emits = defineEmits(['toggleUnit'])
</script>

<template>
  <div class="container mx-auto px-4">
    <div class="flex flex-col border rounded items-center justify-center p-12">
      <p>
        Current distance from the North pole
      </p>
      <h2>{{ `${distance} ${unit}` }}</h2>
      <button class="mt-4 bg-red-500 hover:bg-red-700 text-white py-2 px-4 rounded" @click="$emit('toggleUnit')">
        {{ `Switch to ${unit !== 'km' ? 'km' : 'mile' }` }}
      </button>
    </div>
  </div>
</template>