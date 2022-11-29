<template>
  <v-app>
    <v-main>
      <Main></Main>
      <ReloadPrompt />
    </v-main>
  </v-app>
</template>

<script setup>
  import Main from '@/components/Main.vue'
  import ReloadPrompt from './ReloadPrompt.vue'
</script>