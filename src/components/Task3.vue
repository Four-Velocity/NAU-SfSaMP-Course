<template>
  <v-card>
    <v-card-text>
      <v-img
        v-if="lang === 'uk'"
        :src="`../../public/res/uk/CoA.png`"
        width="200px"
      ></v-img>
      <v-img
        v-else-if="lang === 'en'"
        :src="`../../public/res/en/CoA.png`"
        width="200px"
      ></v-img>
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