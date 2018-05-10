<template>
  <div class="row">
    <quote v-for="x in quotes">{{x}}</quote>
  </div>
</template>

<script>
  import Quote from "./Quote";
  export default {
    name: "QuoteGrid",
    components: {Quote},
    props:{
      quotes:{
        type:Array
      }
    }
  }
</script>

<style scoped>
</style>
