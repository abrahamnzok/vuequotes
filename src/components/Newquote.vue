<template>
  <div class="row">
    <form>
          <div class="form-group">
            <label>Quote</label>
              <textarea class="form-control rounded-0" rows="10" v-model="quote"></textarea>
          </div>
      <div class="col-md-8 col-md-6">
        <button class="btn btn-primary" @click.prevent="create">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    name: "Newquote",
    data:function () {
      return {
        quote:''
      }
    },
    methods:{
      create(){
        this.$emit('oncreation', this.quote);
        this.quote = '';
      }
    }
  }
</script>

<style scoped>
</style>
