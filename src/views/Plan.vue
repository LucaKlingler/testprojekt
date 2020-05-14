<template>
  <div>
    <dropdown :dropdownFacts="days"></dropdown>

    <br>
    <list :listFacts="loadedData.data"></list>

  </div>
</template>

<script>
  import dropdown from "../components/dropdownvue.vue"
  import list from "../components/list.vue"
  import axios from "axios"

  export default {
    name: 'Plan',
    components: {
      dropdown, list
    },
    props: {
      msg: String
    },
    data: function(){
      return {
        loadedData: "",
        days: ["Mo", "Di", "Mi", "Do", "Fr"]
      }
    },
    mounted () {
      axios.get("http://localhost:3000/api/getData")
      .then(response => {
        this.loadedData = response
        this.dropdownData = this.loadedData.map((essen) => essen.day);
        this.dropdownData = this.dropdownData.filter((a, b) => this.dropdownData.indexOf(a) === b)
      })
      .catch(err => {
        console.log(err)
      })
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>