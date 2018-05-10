<template>
  <div class="row">
    <quote v-for="(quote, index) in quotes" :key="quote.id" @click.native="deleteQuote(index)">{{quote}}}</quote>
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
    },
    methods:{
      deleteQuote(index){
        this.$emit('quoteDeleted', index);
      }
    }
  }
</script>

<style scoped>
</style>
