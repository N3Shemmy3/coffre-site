<script setup lang="ts">
import {useLenis, VueLenis} from 'lenis/vue'
import type Lenis from "lenis";
import Header from "~/components/Header.vue";


const scrollCallback = (lenis: Lenis) => {
  // called on every scroll
  // useLenis provides the lenis instance as an argument
}

const lenis = useLenis(scrollCallback, 0) // where 0 is the default callback priority
</script>

<template>
  <VueLenis root/>
  <div class="flex flex-col w-dvw overflow-auto overflow-y-scroll">

    <Header/>

    <main class="flex flex-col gap-8 pb-14">
      <section>
        <Container class="flex flex-col gap-4 md:gap-6 xl:gap-8">
          <label class="font-medium md:text-base">Status: <strong>Rewriting(Design Phase)</strong></label>

          <div>
            <h2 class="font-bold text-3xl md:text-4xl lg:text-6xl tracking-tighter md:mb-4">
              Coffre: <br/>
              Personal finance made simple
            </h2>
            <p class="md:text-lg max-w-150">
              Track your income, expenses, and transfers with ease & gain insights into your spending habits,
              and achieve your financial goals.</p>
          </div>

        </Container>
      </section>

      <section>
        <Container>
          <div class="flex flex-col gap-2">
            <h4 class="text-2xl md:text-2xl lg:text-4xl tracking-tighter">
              Progress
            </h4>
            <p class="md:text-lg max-w-150">
              Currently in the design phase of development and will very quickly start development once completed.
            </p>
          </div>

          <ol class="grid grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-2 md:gap-4 xl:gap-6 mt-4 md:mt-6 lg:mt-8">
            <li v-for="n in 9" class="rounded-lg overflow-clip w-full aspect-9/16 ">
              <img :src="'/img/'+n+'.webp'" alt="screen design">
            </li>
          </ol>
        </Container>
      </section>
    </main>

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
  font-feature-settings: on;
  font-kerning: normal;
  letter-spacing: -0.4px;
}
</style>
