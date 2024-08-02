<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Menubar from 'primevue/menubar';
import { ref } from 'vue';


const items = ref<{ label: string, route?: string }[]>([
  { label: 'Home', route: '/' },
  { label: 'About', route: '/about' },
  { label: 'Contact', route: '/contact' },
])

</script>

<template>
  <header>

    <Menubar :model="items">
      <template #item="{ item }">

      </template>
    </Menubar>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />


    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
