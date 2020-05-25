<template>
  <div>
    <table>
      <th>Kategorie</th>
          <th>Infos</th>
          <th>Kosten</th>
          <th>Tag</th>
          <th>Downvotes</th>
          <th>ID</th>
          <th>Labels</th>
          <th>Name</th>
          <th>Upvotes</th>
    </table> 
    <meals v-for="mealsFromtTable in tableData" :key="mealsFromtTable" :meals="mealsFromtTable"></meals>
  </div>
</template>
<script>
import meals from "../components/meals.vue"
  export default {
    name: 'list',s
    props: {
      tableData: String
    }, 
    components: {
      meals
    }
  }
  
</script>
<style scoped>
.mahlzeit {
  margin-bottom: 20px;
  background-color:aquamarine;
}
</style>