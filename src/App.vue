<template>
  <div id="app" class="container">
    <QuoteGrid :quotes="quotes"/>
  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";

  export default {
    name: 'App',
    components: {QuoteGrid},
    data: function () {
      return {
        quotes: ['No tablecloths, silver cutlery, fine porcelain, sommeliers, or deep wine lists - that\'s fine. But no service or hospitality? That\'s going too far\n'],
        limit: 10,
        info: "You will need to only click on the quote to delete it"
      }
    }
  }
</script>

<style>
  @import "../node_modules/bootstrap/dist/css/bootstrap-grid.min.css";

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
