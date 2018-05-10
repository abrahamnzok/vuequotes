<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Quote"
    }
</script>

<style scoped>
  .panel-body{
    font-family: "Open Sans",serif;
    background-color: aliceblue;
    font-size: 18px;
    color: #034561;
  }
  .quote{
    cursor: pointer;
    padding: 3%;
  }
  .quote:hover{
    border: 1px solid #4FB783;
  }
</style>
