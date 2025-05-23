<script setup lang="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
function onLogin() {
  console.log('login')
  router.replace('/')
}
</script>

<template>
  <form @submit.prevent="onLogin">
    <div class="mb-4">
      <label for="username" class="block text-gray-600">Username</label>
      <input type="text" id="username" name="username" class="w-full border border-gray-300 rounded-md py-2 px-3" />
    </div>
    <div class="mb-4">
      <label for="password" class="block text-gray-600">Password</label>
      <input type="password" id="password" name="password" class="w-full border border-gray-300 rounded-md py-2 px-3" />
    </div>
    <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 w-full">Login</button>
    <div class="mt-6 text-blue-500 text-center">
      <router-link to="/auth/register" class="hover:underline">Sign up Here</router-link>
    </div>
  </form>
</template>
