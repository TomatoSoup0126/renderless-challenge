<script setup>
import NorthPoleDistance from './components/NorthPoleDistance.vue'
import ExampleOne from './components/ExampleOne.vue'
import ExampleTwo from './components/ExampleTwo.vue'
</script>

<template>
  <div class="container mx-auto px-4">
    <h2>Example 1</h2>
    <NorthPoleDistance v-slot="{ distance, unit, toggleUnit }">
      <ExampleOne
        :distance="distance"
        :unit="unit"
        @toggle-unit="toggleUnit"
      />
    </NorthPoleDistance>

    <h2 class="mt-16">Example 2</h2>
    <NorthPoleDistance v-slot="{ distance, unit, toggleUnit }">
      <ExampleTwo
        :distance="distance"
        :unit="unit"
        @toggle-unit="toggleUnit"
      />
    </NorthPoleDistance>
  </div>
</template>
