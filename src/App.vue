<template>
  <div id="app" class="container">
    <div class="col-lg-12">
      <newquote @oncreation="createQuote"/>
    </div>
    <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuotes"/>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          {{info}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";
  import Newquote from "./components/Newquote";

  export default {
    name: 'App',
    components: {Newquote, QuoteGrid},
    data: function () {
      return {
        quotes: ['No tablecloths, silver cutlery, fine porcelain, sommeliers, or deep wine lists - that\'s fine. But no service or hospitality? That\'s going too far\n'],
        limit: 10,
        info: "You will only need to  click on the quote to delete it"
      }
    },
    methods: {
      createQuote(quote) {
        this.quotes.push(quote);
      },
      deleteQuotes(index) {
        this.quotes.splice(index, 1);
      }
    }
  }
</script>

<style>
  @import '../node_modules/bootstrap/dist/css/bootstrap.css';
  @import '../node_modules/bootstrap-vue/dist/bootstrap-vue.css';

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
