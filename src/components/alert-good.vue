<template>
  <v-alert
      border="top"
      colored-border
      elevation="2"
      outlined
      v-show="showSucsess"
  >
    Данные врача добавлены в последний день смен </v-alert>
</template>

<script>
export default {
  name: "alert-good",
  props:{
    showSucsess:Boolean
  }
}
</script>

<style scoped>

</style>
