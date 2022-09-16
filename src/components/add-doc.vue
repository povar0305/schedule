<template>
  <v-row
      class="form">
    <div class="form_add">
      <v-text-field
          label="Имя"
          :rules="rules"
          hide-details="auto"
      ></v-text-field>
      <v-text-field
          label="Фамилия"
          :rules="rules"
          hide-details="auto"
      ></v-text-field>
      <v-text-field
          label="Отчество"
          :rules="rules"
          hide-details="auto"
      ></v-text-field>
      <v-btn
          elevation="2"
          outlined
          plain
          rounded
          text
      >Сохранить
      </v-btn>
    </div>
  </v-row>
</template>

<script>
export default {
  name: "add-doc"
}
</script>

<style lang="scss">
.form {
  justify-content: center;
  padding-bottom: 30px;
  padding-top: 30px;

  &_add {
    display: flex;
    flex-direction: column;
  }

  & button {
    margin-top: 15px;
  }

  & .theme--light.v-btn.v-btn--outlined.v-btn--text {
    background-color: #B5D9FD;
  }
}
</style>
