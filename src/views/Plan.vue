<template>
<div>
<h1>Full-Stack</h1>
    <span>Wochentag</span>
  <select name="Wochentag" id="selectBox">
          <option>Montag</option>
          <option>Dienstag</option>
          <option>Mittwoch</option>
          <option>Donnerstag</option>
          <option>Freitag</option>
        </select>
    
        <br>
    
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
  name: 'Plan',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
