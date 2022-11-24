<template>
  <v-toolbar color="primary">
    <v-toolbar-title> Лабораторна робота №1 </v-toolbar-title>

    <v-spacer></v-spacer>

    {{ sem_mapping[lang] }}
    <v-btn @click="lang = 'en'" v-if="lang === 'uk' || !lang">
      <v-img src="../../public/res/uk/Flag.svg" width="40px"></v-img>
    </v-btn>

    <v-btn @click="lang = 'uk'" v-else-if="lang === 'en'">
      <v-img src="../../public/res/en/Flag.svg" width="40px"></v-img>
    </v-btn>

    <template v-slot:extension>
      <v-tabs v-model="tab" fixed-tabs color="secondary">
        <v-tab value="one">Завдання №1</v-tab>
        <v-tab value="two">Завдання №2</v-tab>
        <v-tab value="three">Завдання №3</v-tab>
      </v-tabs>
    </template>
  </v-toolbar>

  <v-window v-model="tab" class="text-center">
    <v-window-item value="one">
      <Task1 />
    </v-window-item>

    <v-window-item value="two">
      <Task2 :lang="lang" />
    </v-window-item>

    <v-window-item value="three">
      <Task3 :lang="lang" />
    </v-window-item>
  </v-window>
</template>

<script>
import Task1 from "@/components/Task1.vue";
import Task2 from "@/components/Task2.vue";
import Task3 from "@/components/Task3.vue";

export default {
  data: () => ({
    tab: null,
    lang: "uk",
    sem_mapping: {
      uk: "Українська",
      en: "English",
    },
  }),
  components: {
    Task1,
    Task2,
    Task3,
  },
};
</script>