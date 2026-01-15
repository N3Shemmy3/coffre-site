<script setup lang="ts">
import {useLenis, VueLenis} from 'lenis/vue'
import type Lenis from "lenis";


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


const scrollCallback = (lenis: Lenis) => {
  // called on every scroll
  // useLenis provides the lenis instance as an argument
}

const lenis = useLenis(scrollCallback, 0) // where 0 is the default callback priority
</script>

<template>
  <VueLenis root/>
  <div class="flex flex-col w-dvw overflow-auto overflow-y-scroll">

    <header class="flex flex-col px-6 py-2 md:px-16 2xl:py-24 2xl:px-8 pt-60">
      <nav class="w-full *:h-fit grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 xl:grid-cols-6 2xl:grid-cols-12">

        <div id="contribution" class="flex flex-col gap-2">
          <p class="font-medium">Contribute</p>
          <ol id="contribution-list" class="flex flex-col gap-0.5">
            <NuxtLink
                v-for="link in links"
                :key="link.title"
                :to="link.url"
                target="_blank"
                class="flex gap-1 group"
            >
              <Icon class="hidden group-hover:flex size-8" name="ic:arrow-right"/>
              <p class="text-lg"> {{ link.title }}</p>
            </NuxtLink>
          </ol>
        </div>

        <div id="socials" class="flex flex-col gap-2">
          <p class="font-medium">Socials</p>
          <ol id="socials-list" class="flex flex-col gap-0.5">
            <NuxtLink
                v-for="link in socials"
                :key="link.title"
                :to="link.url"
                target="_blank"
                class="flex gap-1 group"
            >
              <Icon class="hidden group-hover:flex size-8" name="ic:arrow-right"/>
              <p class="text-lg"> {{ link.title }}</p>
            </NuxtLink>
          </ol>
        </div>

      </nav>
    </header>

    <div v-for="n in 100" class="h-40">
    </div>

  </div>
</template>

<style>
body {
  height: 100dvh;
  width: 100dvw;
  background: var(--color-colorBackground);
  color: var(--color-colorOnBackground);
  margin: 0;
  padding: 0;
}
</style>
