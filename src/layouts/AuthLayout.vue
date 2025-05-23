<!-- src/layouts/AuthLayout.vue -->
<template>
  <div class="auth-layout">
    <header class="text-center my-4">
      <h1>Bienvenido</h1>
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>

<style scoped>
.auth-layout {
  max-width: 400px;
  margin: 0 auto;
  padding: 2rem;
}
</style>
