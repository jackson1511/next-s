<template>
  <div>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/blog">Blog</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/auth/login">Login</NuxtLink>
        </li>
      </ul>
    </nav>
    <main>
      <slot />
    </main>
  </div>
</template>
