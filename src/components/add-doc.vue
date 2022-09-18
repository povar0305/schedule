<template>
  <v-row
      class="form">
    <div class="form_add">
      <v-alert
          color="indigo"
          type="error"
          outlined
          text
          :value="showModal"
      >Введите все данные</v-alert>
      <v-text-field
          label="Имя"

          hide-details="auto"
          v-model="inputName"
      ></v-text-field>
      <v-text-field
          label="Фамилия"

          hide-details="auto"
          v-model="surname"

      ></v-text-field>
      <v-text-field
          label="Отчество"

          hide-details="auto"
          v-model="nameF"

      ></v-text-field>
<v-col>
  <v-btn
      @click="checkInfo"
      elevation="2"
      outlined
      plain
      rounded
      text
      type="submit"
  >Сохранить
  </v-btn>


</v-col>

    </div>

  </v-row>
</template>

<script>
export default {
  name: "add-doc",
  data(){
    return{
      inputName:'',
      surname:'',
      nameF:'',
      showModal:false

    }
  },
  methods:{
    checkInfo(){
      if(!this.inputName && !this.surname && !this.nameF){
        this.showModal=true
      }else{
        // todo добавление в массив - передача в родительский элемент
      }
    }
  }
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
.v-alert__icon{
  border: none !important;
}
.v-alert--text:before{
  background-color: #ff7676;
  opacity: 0.5;
}
</style>
