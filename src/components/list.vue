<template>
<b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
    <b-carousel-slide class="slide" v-for="meals in mahlzeiten" :key="meals" img-src="https://picsum.photos/1024/480/?image=52"
      ><meals class='mahlzeit' :data="meals"></meals></b-carousel-slide>
</b-carousel>
</template>

<script>
import meals from "../components/meals.vue"
  export default {
    props: {
      mahlzeiten: Array
    }, 
    components: {
      meals
    },
    name: 'list'
  }
</script>

<style scoped>
.mahlzeit {
  margin-bottom: 50px;
  max-width: 500px;
  margin-left:auto;
  margin-right:auto;
}
</style>