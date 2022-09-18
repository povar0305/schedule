<template>
  <v-col class="table">

    <v-col class="table_main">
      <gallery-days @selectDate="selectDate" :date="date"></gallery-days>
      <alert-good :showSucsess="showSucsess"></alert-good>
      <v-row
          class="table_main--title m-0"
          justify="end">
        <v-col class="first">&nbsp;</v-col>
        <v-col>00</v-col>
        <v-col>01</v-col>
        <v-col>02</v-col>
        <v-col>03</v-col>
        <v-col>04</v-col>
        <v-col>05</v-col>
        <v-col>06</v-col>
        <v-col>07</v-col>
        <v-col>08</v-col>
        <v-col>09</v-col>
        <v-col>10</v-col>
        <v-col>11</v-col>
        <v-col>12</v-col>
        <v-col>13</v-col>
        <v-col>14</v-col>
        <v-col>15</v-col>
        <v-col>16</v-col>
        <v-col>17</v-col>
        <v-col>18</v-col>
        <v-col>19</v-col>
        <v-col>20</v-col>
        <v-col>21</v-col>
        <v-col>22</v-col>
        <v-col>23</v-col>
      </v-row>

      <table>
        <tbody>
        <tr  >
          <v-row class="table_main_info first"  >
            <td class="table_main_info--surname  " >
            </td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </v-row>

        </tr>
        <tr v-for="elements in selectDate(this.selectDateResult)" :key="String(elements.date)">
          <v-row class="table_main_info" v-for="element in elements.dateInner" :key="element.surname">
            <td class="table_main_info--surname "  >
              <a :href='"?surname=" + element.surname'>{{ element.surname }} {{ element.NF }}</a>
            </td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </v-row>
        </tr>
        </tbody>
      </table>
    </v-col>

    <add-doc @addDocInfo="addDocInfo"></add-doc>
  </v-col>

</template>

<script>
import galleryDays from "@/components/gallery-days";
import AddDoc from "@/components/add-doc";
import AlertGood from "@/components/alert-good";

export default {
  name: "tableMain",
  components: {
    AlertGood,
    AddDoc,
    galleryDays,
  },
  data() {
    return {
      selectDateResult: new Date(2025, 10, 6),
      showSucsess:false,

      date: [
        {
          date: new Date(2025, 10, 6),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 7),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 8),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 9),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              },
              ]
        },
        {
          date: new Date(2025, 10, 10),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 11),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 12),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 13),

          dateInner:

              [
                {

                  surname: 'Ульянов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'О. Н.'
                }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 14),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 15),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: ' М. Т.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 16),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 17),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: this.random(4, 12),
                  startWork: this.random(0,23),
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. Н.'
              }, {

                surname: 'Ермолаев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {


                surname: 'Куликова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: this.random(4, 12),
                startWork: this.random(0,23),
                NF: 'О. А.'
              }
              ]
        },
      ]
    }
  },

  methods: {
    selectDate(e) {
      if (typeof (e) !== 'undefined') {
        this.selectDateResult = e
      }
      return this.date.filter(el => {
        if (el.date.getTime() == this.selectDateResult.getTime()) {
          return el
        }
      })
    },
    random(min, max) {
      return Math.floor(min + Math.random() * (max - min));
    },
    addDocInfo(e){
      let newStartWork=this.random(0,23-e.countHour)
      e.startWork = newStartWork
      let lastItem = this.date[this.date.length-1]
      lastItem.dateInner.push(e)
      this.showSucsess=true
      window.scrollTo(top)
    }

  },
  /*computed: {

    setDate: function () {
      this.selectDate(new Date(2025, 10, 6))
    }
  }*/

}
</script>

<style lang="scss" scoped>
.table {
  justify-content: center !important;
  display: flex;
  flex-direction: column;
  align-items: center;

  &_main {
    max-width: 1124px;
    margin-top: 24px;

    &--title {
      width: 100%;
      justify-content: end;
      margin: 0;

      & .col {
        border: 1px solid #E3EFF9;
        height: 40px;
        padding: 0;
        width: 38px;
        display: flex;
        align-items: center;
        justify-content: center;
        max-width: 40px;
        text-align: center;
        font-weight: 500;
        font-size: 12px;
        line-height: 150%;
        color: #636363;

        &.first {
          flex: 1;
          width: 100%;
          min-width: 180px;
        }
      }
    }

    & table {
      border-collapse: collapse;
      display: flex;
      justify-content: center;

      & tbody {
        width: 100%;

      }

      & td, & tbody {
        border: 1px solid #E3EFF9;
      }


      & a {
        padding-left: 20px;
        color: black;
      }
    }

    &_info {
      position: relative;
      width: 100%;
      margin: 0;

      & td {
        width: 38.31px;
        border-top: none !important;
        border-bottom: none !important;
      }
      &.first{

        &:hover {
          background-color: transparent !important;
        }
        & td{
          border: 1px solid #E3EFF9;
          height: 24px;
        }
      }
      &:hover {
        background-color: #B5D9FD !important;
        border-radius: 30px;
      }

      &--surname {
        border-bottom: none !important;
        border-top: none !important;
        min-width: 167px;
        width: 100%;
        flex: 1;
        position: relative;

        & a {
          font-weight: 500;
          font-size: 12px;
          line-height: 150%;
        }


        &.true::after {
          content: '';
          position: absolute;
          height: 10px;
          border-radius: 20px;
          background-color: #47E69A;
          min-width: 160px;
          right: -163px;
        }
      }
    }

  }
}


</style>
