<script setup>
// import { RouterLink } from 'vue-router';
import Input from '@/components/Input/Input.vue';
import { ref } from 'vue';
import { RouterLink } from 'vue-router';

const form = ref({
  email: '',
  password: ''
});

</script>

<template>
  <form>
    <Input
      placeholder="Type your email"
      id="email"
      type="email"
      name="email"
      forLabel="email"
      labelName="Email Addres"
      v-model:modelValue="form.email"
    />
    <Input
      placeholder="Type your password"
      id="password"
      type="password"
      name="password"
      forLabel="password"
      labelName="Password"
      v-model:modelValue="form.password"
    />
    <div class="mt-6">
      <RouterLink to="/"
        class="inline-flex items-center justify-center w-full px-8 py-3 text-base font-medium text-white bg-yellow-500 border border-transparent rounded-full hover:bg-yellow-600 md:py-2 md:text-lg md:px-10 hover:shadow">
        Sign In
      </RouterLink>
      <RouterLink to="/register"
        class="inline-flex items-center justify-center w-full px-8 py-3 mt-2 text-base font-medium text-black bg-gray-200 border border-transparent rounded-full hover:bg-gray-300 md:py-2 md:text-lg md:px-10 hover:shadow">
        Create New Account
      </RouterLink>
    </div>
  </form>
</template>