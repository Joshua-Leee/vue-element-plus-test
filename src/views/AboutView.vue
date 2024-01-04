<script setup>
import { ref } from 'vue'
const options = [
  {
    value: 'Option1',
    label: 'Option1',
  },
  {
    value: 'Option2',
    label: 'Option2',
  },
  {
    value: 'Option3',
    label: 'Option3',
  },
  {
    value: 'Option4',
    label: 'Option4',
  },
  {
    value: 'Option5',
    label: 'Option5',
  },
]

const value = ref()
const value4 = ref()
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div>
      <el-select v-model="value" class="m-2" placeholder="Select">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value" />
      </el-select>
    </div>
    <div class="block">
      <span class="demonstration">Dates</span>
      <el-date-picker
        v-model="value4"
        type="dates"
        placeholder="Pick one or more dates" />
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
}
</style>
