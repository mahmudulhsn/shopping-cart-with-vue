<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="bg-slate-800 text-white">
    <div class="container mx-auto">
      <div class="flex py-5">
        <header class="w-5/6 ">
          <nav>
            <RouterLink to="/" class="p-5 bg-gray-500 hover:bg-teal-900 transition duration-300 ease-in-out">
              Home
            </RouterLink>
            <RouterLink to="/about" class="p-5 bg-gray-500 hover:bg-teal-900 transition duration-300 ease-in-out">About
            </RouterLink>
            <RouterLink to="/test" class="p-5 bg-gray-500 hover:bg-teal-900 transition duration-300 ease-in-out">Test
            </RouterLink>
          </nav>
        </header>
      </div>
    </div>
  </div>

  <div class="container mx-auto">
    <RouterView />
  </div>

</template>

<style>
/* @import "@/assets/base.css"; */
</style>
