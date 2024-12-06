<template>
  <div>
    <p class="mb-10">Take a look at my GitHub projects!</p>
    <section>
      <p v-if="loading">Loading...</p>
      <p v-else-if="error">Something went wrong... please try again</p>
      <ul v-if="data" class="grid grid-cols-1 gap-4">
        <li
          v-for="repo in repos"
          :key="repo.id"
          class="border borgray-200 rounded-sm hover:bg-gray-100 font-mono p-4"
        >
          <a :href="repo.html_url" target="_blank">
            <div class="flex items-center justify-between">
              <div class="font-bold">
                {{ repo.name }}
              </div>
              <div>{{ repo.stargazers_count }} *</div>
            </div>
            <p class="text-sm">{{ repo.description }}</p>
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
// console.log(
//   await $fetch("https://api.github.com/users/piotr-jura-udemy/repos")
// );
const { data, error, loading } = await useFetch(
  "https://api.github.com/users/piotr-jura-udemy/repos"
);

const repos = computed(() =>
  data.value
    .filter((repo) => repo.description)
    .sort((a, b) => b.stargazers_count - a.stargazers_count)
);
</script>
