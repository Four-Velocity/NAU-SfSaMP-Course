<template>
  <v-card>
    <v-card-text>{{
      lang === "uk" || !lang ? ukText.fullname : enText.fullname
    }}</v-card-text>
  </v-card>
</template>

<style scoped>
.v-card-text {
  font-style: italic;
  font-size: 23px;
  color: rgb(255, 204, 0);
}
</style>

<script>
import enText from "../../public/res/en/text.json";
import ukText from "../../public/res/uk/text.json";

export default {
  props: ["lang"],
  data: () => ({
    enText: enText,
    ukText: ukText,
  }),
};
</script>