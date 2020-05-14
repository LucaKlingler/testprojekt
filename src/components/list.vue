<template>
  <div>
    <table>
      <tr>Snack</tr>
      <tr>Tagessuppe</tr>
      <tr>Hauptgericht</tr>
      <tr>Dessert</tr>
    </table> 
    <div class="mahlzeit" v-for="meal in listFacts" :key="meal">{{meal}}</div>
    <!--{{listFacts}}-->
  </div>
</template>
<script>
  export default {
    name: 'list',
    props: {
      listFacts: Object
    }
  }
</script>
<style scoped>
.mahlzeit {
  margin-bottom: 20px;
  background-color:aquamarine;
}
</style>