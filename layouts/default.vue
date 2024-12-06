<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center mt-5 p-2">
      <div class="flex items-center space-x-12">
        <div>
          <NuxtLink to="/" class="text-xl font-semibold hover:bg-gray-200"
            >JACKSON</NuxtLink
          >
        </div>
        <Menu />
      </div>

      <!-- <ColorModeSelector /> -->
    </header>

    <main class="p-2 mb-10">
      <slot />
    </main>
  </div>
</template>

<script setup>
useHead({
  titleTemplate: "%s | Jackson",
  link: [
    {
      rel: "preconnect",
      href: "https://fonts.googleapis.com",
    },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Roboto&display=swap",
      crossorigin: "",
    },
  ],
});
</script>

<style>
body {
  @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300;
}
body {
  font-family: "Roboto";
}
</style>
