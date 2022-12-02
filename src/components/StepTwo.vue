<template>
  <div class='grid gap-4'>
    <div class="font-semibold flex items-center justify-between -mt-7 mb-5">
      <p class="text-lg">Academic Details </p>
      <p>Step 2/3</p>
    </div>
    <div class="flex gap-4 flex-col sm:flex-row">
      <input type="text" placeholder="Institution Name">
      <input type="text" placeholder="Course of Study">
    </div>
    <div class="">
      <input class="w-full" type="email" placeholder="Email Address">
    </div>
    <div class="flex gap-4">
      <input class="" type="text" placeholder="Year of Admission">
      <input class="" type="text" placeholder="Year of Graduation">
    </div>
    <div class="flex justify-center gap-4">
      <button class="bg-blue-500 px-8 py-2 rounded-sm text-white mt-5" @click="nextStep('StepOne')"> Previous
        Step</button>
      <button class="bg-blue-500 px-8 py-2 rounded-sm text-white mt-5" @click="nextStep('StepThree')"> Next
        Step</button>
    </div>
  </div>
</template>
<script setup>
import { inject } from 'vue';
const nextStep = inject('nextStep');

</script>
<style>

</style>