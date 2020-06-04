<template>
      <tr>
          <th>{{meals.category}}</th>
          <td>{{meals.contentInformation}}</td>
          <td>{{meals.cost}}</td>
          <td>{{meals.day}}</td>
          <td>{{meals.downvotes}}</td>
          <td>{{meals.id}}</td>
          <td>{{meals.labels}}</td>
          <td>{{meals.name}}</td>
          <td>{{meals.upvotes}}</td>
      </tr>
</template>

<script>
export default {
  name: 'meals',
  props: {
    meals: Object
  }
}
</script>

<style scoped>
* {
  text-align: left;
}


.ci {
  font-size: 8px;
  display: inline-block;
  margin-right:10px;
}
</style>