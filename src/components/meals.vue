<template>
<div>
<table>
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
</table>
</div>
</template>

<script>
  export default {
    name: 'meals',
    props: {
      meals: Object
    }
  }

</script>