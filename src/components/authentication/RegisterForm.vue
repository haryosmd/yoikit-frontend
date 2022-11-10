<script setup>
// import { RouterLink } from 'vue-router';
import Input from '@/components/Input/Input.vue';
import { ref } from 'vue';
import { RouterLink } from 'vue-router';

const form = ref({
  name: '',
  email: '',
  password: ''
});

</script>

<template>
  <form>
    <Input placeholder="Type your full name" id="name" type="text" name="name" forLabel="name" labelName="Name"
      v-model:modelValue="form.name" />
    <Input placeholder="Type your email" id="email" type="email" name="email" forLabel="email" labelName="Email Addres" v-model:modelValue="form.email" />
    <Input placeholder="Type your password" id="password" type="password" name="password" forLabel="Password" labelName="password" v-model:modelValue="form.password" />
    <div class="mt-6">
      <RouterLink to="/"
        class="inline-flex items-center justify-center w-full px-8 py-3 text-base font-medium text-white bg-yellow-500 border border-transparent rounded-full hover:bg-yellow-600 md:py-2 md:text-lg md:px-10 hover:shadow">
        Continue Sign Up
      </RouterLink>
      <RouterLink to="/login"
        class="inline-flex items-center justify-center w-full px-8 py-3 mt-2 text-base font-medium text-black bg-gray-200 border border-transparent rounded-full hover:bg-gray-300 md:py-2 md:text-lg md:px-10 hover:shadow">
        Sign In
      </RouterLink>
    </div>
  </form>
</template>