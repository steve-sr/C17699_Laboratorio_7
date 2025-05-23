<script setup lang="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
function onRegister() {
  console.log('register')
  router.replace('/')
}
</script>

<template>
  <form @submit.prevent="onRegister">
    <div class="mb-4">
      <label for="name" class="block text-gray-600">Name</label>
      <input type="text" id="name" class="w-full border border-gray-300 rounded-md py-2 px-3" />
    </div>
    <div class="mb-4">
      <label for="email" class="block text-gray-600">Email</label>
      <input type="email" id="email" class="w-full border border-gray-300 rounded-md py-2 px-3" />
    </div>
    <div class="mb-4">
      <label for="password" class="block text-gray-600">Password</label>
      <input type="password" id="password" class="w-full border border-gray-300 rounded-md py-2 px-3" />
    </div>
    <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 w-full">Register</button>
    <div class="mt-6 text-blue-500 text-center">
      <router-link to="/auth/login" class="hover:underline">Already have an account? Login</router-link>
    </div>
  </form>
</template>
