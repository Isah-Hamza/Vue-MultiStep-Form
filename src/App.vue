<template>
  <div class='grid h-screen w-screen place-content-center'>
    <h4 class="text-2xl font-semibold mb-5 text-center">Multi-step Form</h4>
    <div class="grid place-content-center border rounded-md p-10 bg-white">
      <div class="mt-5">
        <keep-alive>
          <component :is="activeStep" />
        </keep-alive>
        <!-- <StepOne />
        <StepTwo />
        <StepThree /> -->
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, provide, computed } from 'vue';
import StepOne from './components/StepOne.vue';
import StepTwo from './components/StepTwo.vue';
import StepThree from './components/StepThree.vue';

// data
const currentStep = ref("StepOne");

// computed values
const activeStep = computed(() => {
  const steps = {
    'StepOne': StepOne,
    'StepTwo': StepTwo,
    'StepThree': StepThree,
  }
  return steps[currentStep.value];
})

// methods
const nextStep = (step) => {
  console.log(step)
  currentStep.value = step;
};

// provide
provide('nextStep', nextStep);

</script>
<style>

</style>