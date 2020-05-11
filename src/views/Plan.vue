<template>
  <div>
    {{loadedData}}
    <dropdown></dropdown>

    <br>
    <list></list>

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
      }
    },
    mounted () {
      axios.get("http://localhost:3000/api/getData")
      .then(response => {
        this.loadedData = response
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