<template>
  <v-col>
    <v-col class="table_main">
      <gallery-days :date="date"></gallery-days>
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

        <tr v-for="element in this.date" :key="element.id" class="table_main_info" >
          <td class="table_main_info--surname " v-bind:class="{ first: element.id==0 }">
            <a :href='"?surname=" + element.surname'>{{ element.surname }} {{ element.NF }}{{element.id}}</a>
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
        </tr>
        </tbody>
      </table>
    </v-col>
<add-doc></add-doc>  </v-col>

</template>

<script>
import galleryDays from "@/components/gallery-days";
import AddDoc from "@/components/add-doc";

export default {
  name: "tableMain",
  components: {
    AddDoc,
    galleryDays
  },
  data() {
    return {
      date: [
          {
        id:0,
        date: new Date(2025, 10, 6),
        surname: 'Борисов',
        countHour: 4,
        startWork: '01',
        NF:'Д. Н.'
      }, {
        id:1,
        date: new Date(2025, 10, 7),
        surname: 'Воробьев',
        countHour: 4,
        startWork: '01',
        NF:'К. С.'
      }, {
        id:2,
        date: new Date(2025, 10, 8),
        surname: 'Ульянов',
        countHour: 4,
        startWork: '01',
        NF:'О. Н.'
      }, {
        id:3,
        date: new Date(2025, 10, 9),
        surname: 'Антипова',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:4,
        date: new Date(2025, 10, 10),
        surname: 'Зайцев',
        countHour: 4,
        startWork: '01',
        NF:'К. Е.'
      }, {
        id:5,
        date: new Date(2025, 10, 11),
        surname: 'Ермолаев',
        countHour: 4,
        startWork: '01',
        NF:'Д. И.'
      }, {
        id:6,
        date: new Date(2025, 10, 12),
        surname: 'Еремеева',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:7,
        date: new Date(2025, 10, 13),
        surname: 'Васильева',
        countHour: 4,
        startWork: '01',
        NF:'С. В.'
      }, {
        id:8,
        date: new Date(2025, 10, 14),
        surname: 'Лебедев',
        countHour: 4,
        startWork: '01',
        NF:'К. С.'
      }, {
        id:9,
        date: new Date(2025, 10, 15),
        surname: 'Васильев',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:10,
        date: new Date(2025, 10, 16),
        surname: 'Потапова',
        countHour: 4,
        startWork: '01',
        NF:' М. Т.'
      }, {
        id:11,
        date: new Date(2025, 10, 17),
        surname: 'Константинова',
        countHour: 4,
        startWork: '01',
        NF:'И. О.'
      }, {
        id:12,
        date: new Date(2025, 10, 18),
        surname: 'Куликова',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:13,
        date: new Date(2025, 10, 19),
        surname: 'Ефремов',
        countHour: 4,
        startWork: '01',
        NF:'Е. Л.'
      }, {
        id:14,
        date: new Date(2025, 10, 20),
        surname: 'Артемова',
        countHour: 4,
        startWork: '01',
        NF:'У. И.'
      }, {
        id:15,
        date: new Date(2025, 10, 21),
        surname: 'Еремин',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:16,
        date: new Date(2025, 10, 22),
        surname: 'Михайлова',
        countHour: 4,
        startWork: '01',
        NF:'И. В.'
      }, {
        id:17,
        date: new Date(2025, 10, 23),
        surname: 'Иванов',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }, {
        id:18,
        date: new Date(2025, 10, 24),
        surname: 'Исаев',
        countHour: 4,
        startWork: '01',
        NF:'Т. И.'
      }, {
        id:19,
        date: new Date(2025, 10, 25),
        surname: 'Федотов',
        countHour: 4,
        startWork: '01',
        NF:'О. А.'
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
.table_main {
  margin-top: 24px;

  & table {
    border-collapse: collapse;
    display: flex;
    justify-content: center;

    & td,& tbody {
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

    & td{
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
      &.first{
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
