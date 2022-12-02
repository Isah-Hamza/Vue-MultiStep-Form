<template>
    <div class='grid gap-4 '>
        <div class="font-semibold flex items-center justify-between -mt-7 mb-5">
            <p class="text-lg">Personal Information </p>
            <p>Step 1/3</p>
        </div>
        <div class="flex gap-4 flex-col sm:flex-row">
            <input type="text" placeholder="First Name">
            <input type="text" placeholder="Last Name">
        </div>
        <div class="">
            <input class="w-full" type="email" placeholder="Email Address">
        </div>
        <div class="flex gap-4">
            <input class="" type="text" placeholder="Phone Number">
            <input class="" type="text" placeholder="Country">
        </div>
        <button class="bg-blue-500 px-8 py-2 rounded-sm text-white mt-5" @click="nextStep('StepTwo')"> Next Step</button>
    </div>
</template>
<script setup>
import { inject } from 'vue';

// injection
const nextStep = inject('nextStep');
</script>
<style>

</style>