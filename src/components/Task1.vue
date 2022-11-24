<template>
  <v-card>
    <v-card-text>
      <Rectangle :height="200" :width="200" :centerX="0" :centerY="0" />
    </v-card-text>
  </v-card>
</template>

<script>
import Rectangle from "@/components/drawable/Rectangle.vue";

export default {
  components: {
    Rectangle,
  },
};
</script>