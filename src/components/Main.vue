<template>
  <v-toolbar>
    <v-toolbar-title> Лабораторна робота №1 </v-toolbar-title>

    <template v-slot:extension>
      <v-tabs v-model="tab" fixed-tabs>
        <v-tab value="one">Завдання №1</v-tab>
      </v-tabs>
    </template>
  </v-toolbar>

  <v-window v-model="tab" class="text-center">
    <v-window-item value="one">
      <Task1 />
    </v-window-item>
  </v-window>
</template>

<script>
import Task1 from "@/components/Task1.vue";

export default {
  data: () => ({
    tab: null,
  }),
  components: {
    Task1,
  },
};
</script>