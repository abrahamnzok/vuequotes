<template>
  <div class="row">
    <div class="col-sm-12">
      <h3>Quotes Package</h3>
      <div class="progress">
        <div class="progress-bar" role="progressbar" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"
          :style="{width: (nQuotes / limit) * 100 + '%'}">
        </div>
        {{nQuotes}} / {{limit}}
      </div>
    </div>
  </div>

</template>

<script>
  export default {
    name: "ProgressBar",
    props:['nQuotes', 'limit']
  }
</script>

<style scoped>

</style>
