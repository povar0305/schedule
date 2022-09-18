<template>
  <v-col>
    <v-col class="table_main">
      <gallery-days @selectDate="selectDate" :date="date"></gallery-days>
      <table>
        <tbody>
        <tr class="table_main--title">
          <td>&nbsp;</td>
          <td>00</td>
          <td>01</td>
          <td>02</td>
          <td>03</td>
          <td>04</td>
          <td>05</td>
          <td>06</td>
          <td>07</td>
          <td>08</td>
          <td>09</td>
          <td>10</td>
          <td>11</td>
          <td>12</td>
          <td>13</td>
          <td>14</td>
          <td>15</td>
          <td>16</td>
          <td>17</td>
          <td>18</td>
          <td>19</td>
          <td>20</td>
          <td>21</td>
          <td>22</td>
          <td>23</td>
        </tr>
        <v-row v-for="elements in selectDate(this.selectDateResult)" :key="String(elements.date)">
          <tr class="table_main_info" v-for="(element,index) in elements.dateInner" :key="element.surname">
            <td class="table_main_info--surname " v-bind:class="{ first: index==0 }">
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
          </tr>

        </v-row>
        </tbody>
      </table>
    </v-col>
    <add-doc></add-doc>
  </v-col>

</template>

<script>
import galleryDays from "@/components/gallery-days";
import AddDoc from "@/components/add-doc";

export default {
  name: "tableMain",
  components: {
    AddDoc,
    galleryDays,
  },
  data() {
    return {
      selectDateResult: new Date(2025, 10, 6),

      date: [
        {
          date: new Date(2025, 10, 6),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 9),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 10),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }
              ]
        },
        {
          date: new Date(2025, 10, 13),

          dateInner:

              [
                {

                  surname: 'Борисов',
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
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
                  countHour: Math.round(4 * Math.random() * 10),
                  startWork: '01',
                  NF: 'Д. Н.'
                }, {

                surname: 'Воробьев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Ульянов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. Н.'
              }, {

                surname: 'Антипова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Зайцев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. Е.'
              }, {

                surname: 'Ермолаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Д. И.'
              }, {

                surname: 'Еремеева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Васильева',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'С. В.'
              }, {

                surname: 'Лебедев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'К. С.'
              }, {

                surname: 'Васильев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Потапова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: ' М. Т.'
              }, {

                surname: 'Константинова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. О.'
              }, {

                surname: 'Куликова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Ефремов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Е. Л.'
              }, {

                surname: 'Артемова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'У. И.'
              }, {

                surname: 'Еремин',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Михайлова',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'И. В.'
              }, {

                surname: 'Иванов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }, {

                surname: 'Исаев',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'Т. И.'
              }, {

                surname: 'Федотов',
                countHour: Math.round(4 * Math.random() * 10),
                startWork: '01',
                NF: 'О. А.'
              }
              ]
        },
      ]
    }
  },

  methods: {
    selectDate(e) {
      console.log("11111111111"+this.selectDateResult)
      if (typeof (e) !== 'undefined') {
        this.selectDateResult = e
      }
      return this.date.filter(el => {
        if (el.date.getTime() == this.selectDateResult.getTime()) {
          return el
        }
      })
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
.table_main {
  margin-top: 24px;

  & table {
    border-collapse: collapse;
    display: flex;
    justify-content: center;

    & td, & tbody {
      border: 1px solid #E3EFF9;

    }

    & .table_main--title td {
      height: 40px;
      padding: 0;
      min-width: 40px;
      text-align: center;
      font-weight: 500;
      font-size: 12px;
      line-height: 150%;
      color: #636363;
    }

    & a {
      padding-left: 20px;
      color: black;
    }
  }

  &_info {
    position: relative;

    & td {
      border-top: 1px solid transparent !important;
      border-bottom: 1px solid transparent !important;
    }

    &:hover {

      background-color: #B5D9FD !important;
      border-radius: 30px;
    }

    &--surname {
      border-bottom: none !important;
      border-top: none !important;
      min-width: 167px;
      position: relative;

      & a {
        font-weight: 500;
        font-size: 12px;
        line-height: 150%;
      }

      &.first {
        padding-top: 24px;
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

</style>
