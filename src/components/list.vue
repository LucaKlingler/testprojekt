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

        <tr v-for="entry in listFacts" :key="entry">
          <th>{{entry.category}}</th>
          <td>{{entry.contentInformation}}</td>
          <td>{{entry.cost}}</td>
          <td>{{entry.day}}</td>
          <td>{{entry.downvotes}}</td>
          <td>{{entry.id}}</td>
          <td>{{entry.labels}}</td>
          <td>{{entry.name}}</td>
          <td>{{entry.upvotes}}</td>
        </tr>
    </table> 
    <!--<div class="mahlzeit" v-for="meal in listFacts" :key="meal">{{meal}}</div>-->
    <!--{{listFacts}}-->
  </div>
</template>
<script>
  export default {
    name: 'list',
    props: {
      listFacts: String
    }
  }
</script>
<style scoped>
.mahlzeit {
  margin-bottom: 20px;
  background-color:aquamarine;
}
</style>