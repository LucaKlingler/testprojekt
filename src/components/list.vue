<template>
  <div>
    <table>
      <tr>Snack</tr>
      <tr>Tagessuppe</tr>
      <tr>Hauptgericht</tr>
      <tr>Dessert</tr>
    </table>
  </div>
</template>
<script>
  export default {
    name: 'list',
    props: {
      data: String
    }
  }
</script>