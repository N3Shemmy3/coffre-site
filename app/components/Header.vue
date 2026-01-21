<script setup lang="ts">

const links = [
  {
    title: "GitHub",
    url: "https://github.com/N3shemmy3/Coffre",
  },
  {
    title: "Figma(wip)",
    url: "https://x.com/N3Shemmy3",
  },
  {
    title: "Donate",
    url: "https://ko-fi.com/n3shemmy3",
  },
]

const socials = [
  {
    title: "Telegram",
    url: "https://t.me/N3shemmy3/",
  },
  {
    title: "X(Twitter)",
    url: "https://x.com/N3Shemmy3",
  },
  {
    title: "Email",
    url: "tel:n3shemmy3@gmail.com",
  },
]
</script>

<template>
  <header class="flex items-center">
    <Container class="flex flex-col">
      <div class="h-14 md:h-28 lg:h-32 xl:h-48"/>
      <nav class="grid gap-4 grid-cols-3 md:grid-cols-6 xl:grid-cols-8">

        <ul class="flex flex-col gap-1">
          <NuxtLink v-for="link in links" :key="link.title" target="_blank" :to="link.url">
            <li class="nav-item">
              {{ link.title }}
            </li>
          </NuxtLink>
        </ul>

        <ul class="flex flex-col gap-1">
          <NuxtLink v-for="link in socials" :key="link.title" target="_blank" :to="link.url">
            <li class="nav-item">
              {{ link.title }}
            </li>
          </NuxtLink>
        </ul>

      </nav>
    </Container>
  </header>
</template>

<style scoped>
.nav-item {
  font-feature-settings: on;
  font-kerning: normal;
  font-size: 18px;
  letter-spacing: -0.4px;
}
</style>