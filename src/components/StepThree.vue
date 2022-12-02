<template>
    <div class='grid gap-4'>
        <div class="font-semibold flex items-center justify-between -mt-7 mb-5">
            <p class="text-lg">Work Experience </p>
            <p>Step 3/3</p>
        </div>
        <div class="flex gap-4 flex-col sm:flex-row">
            <input type="text" placeholder="Last Company Employed">
            <input type="text" placeholder="Designation">
        </div>
        <div class="">
            <input class="w-full" type="email" placeholder="Company Reference Number">
        </div>
        <div class="flex gap-4">
            <input class="" type="text" placeholder="Start Date">
            <input class="" type="text" placeholder="End Date">
        </div>
        <div class="flex justify-center gap-4">
            <button class="bg-blue-500 px-8 py-2 rounded-sm text-white mt-5" @click="nextStep('StepTwo')"> Previous
                Step</button>
            <button class="bg-blue-500 px-8 py-2 rounded-sm text-white mt-5"> Submit</button>
        </div>
    </div>
</template>
<script setup>
import { inject } from 'vue';
const nextStep = inject('nextStep');

</script>
<style>

</style>