<template>
  <div>
    <h1>Willkommen</h1>
    <span>Wochentag</span>
    <select name="Wochentag" id="selectBox">
      <option v-for= "day in dropdownFacts" :key="day">{{day}}</option>
    </select>
  </div>
</template>
<script>
  export default {
    name: 'dropdown',
    props: {
      dropdownFacts: Array
    }
  }
</script>