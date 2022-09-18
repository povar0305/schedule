<template>
  <div id="app">
    <header-block></header-block>
    <table-main></table-main>
  </div>
</template>

<script>
import headerBlock from "@/components/header-block";
import tableMain from "@/components/tableMain";
export default {
  name: 'App',
  components: {
    headerBlock,
    tableMain
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
}
a{
  text-decoration: none;
}
body {
  margin: 0;
}

#app {
  display: flex;
  flex-direction: column;
}

.v-alert{
  background-color:#B5D9FD !important ;
}
</style>
