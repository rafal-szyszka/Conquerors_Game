<template>
  <div class="col-sm-1" style="text-align: center">
    <div v-if="showSplit" class="splitter"></div>
      <img :src="res.imgSource" :alt="res.name" width="28px" height="28px">
      <br>
      {{ res.amount }}
  </div>
</template>

<script>
  export default {
    props: ['res', 'showSplit'],
  }
</script>

<style>

  .splitter {
    border-right: 1px solid whitesmoke;
    float: right;
    height: 45px;
    width: 10px;
  }

</style>
