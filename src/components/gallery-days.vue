<template>
  <v-row class="gallery_row"
  >
    <v-sheet
        class="mx-auto"
        max-width="1128"
    >
      <v-slide-group
          show-arrows
      >
        <v-slide-item
            v-for="n in this.date"
            :key="n.id"
        >

          <div class="gallery_row--item"
          @click="selectedDate(n.date)"  >
            <p>
              <span>
                {{ n.date.getDate() }}.{{ n.date.getMonth() }}
              </span>{{ days[n.date.getDay()] }}
            </p>
          </div>


        </v-slide-item>
      </v-slide-group>
    </v-sheet>

  </v-row>
</template>
<script>


export default {
  name: "gallery-days",
  data: () => ({
    model: null,
    days: ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'],
  }),
  props: {
    date: null

  },
  methods:{
    selectedDate(e){
     console.log(e)
    }
  }
}
;
</script>
<style lang="scss">
.gallery_row {
  justify-content: center;
  margin-top: 42px;
  margin-bottom: 60px;
  &--item{
    &.active,&:hover{
      background: #73AEEA;
      cursor: pointer;
      border-radius: 40px;
      & >*{
        color: white;
      }

    }
    & p{
      padding: 1px 9px;
      font-weight: 500;
      font-size: 14px;
      line-height: 150%;
      color: #636363;

      & span{
        font-weight: 600;
      }
    }

  }
}

.v-icon.v-icon {
  border: 1px solid #73AEEA;
  border-radius: 40px;
  color: #73AEEA;
}
</style>
