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
    <p>{{ `You are current: ${distance} ${unit} away from the North pole` }}</p>
    <button
      class="bg-emerald-500 hover:bg-emerald-700 text-white py-2 px-4 rounded"
      @click="$emit('toggleUnit')"
    >
      Toggle unit
    </button>
  </div>
</template>