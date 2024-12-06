<template>
  <nav>
    <ul class="flex space-x-4">
      <li>
        <NuxtLink to="/" class="link">Home</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about" class="link">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/blog" class="link">Blog</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/project" class="link">Projects</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/auth/login" class="link">Login</NuxtLink>
      </li>
    </ul>
  </nav>
</template>
<style scoped>
.link {
  @apply hover:bg-gray-200;
}
</style>
