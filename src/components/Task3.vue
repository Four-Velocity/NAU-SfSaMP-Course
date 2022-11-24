<template>
  <v-card>
    <v-card-text>
      <v-img :src="`../../public/res/${lang}/CoA.png`" width="200px"></v-img>
    </v-card-text>
  </v-card>
</template>

<style scoped>
.v-img {
  margin: 0 auto;
}
</style>

<script>
export default {
  props: ["lang"],
};
</script>