<template>
  <td class="cnq-resource-item">
    <div class="cnq-resource-item-body">
      <div class="cnq-resource-item-body-content" style="padding: 3px">
        <img :src="imgSource" :alt="name" width="24px" height="24px">
      </div>
      <div class="cnq-resource-item-body-content" style="width: 110px" >
        {{ amount }}
      </div>
    </div>
  </td>
</template>

<script>
  export default {
    props: ['name', 'imgSource', 'amount']
  }
</script>

<style>

  .cnq-resource-item {
    width: 140px;
    padding: 5px;
  }

  .cnq-resource-item-body {
    align-items: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    -webkit-box-align: center;

    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;

    margin: auto;
    text-align: center;
    width: inherit;
  }

  .cnq-resource-item-body-content {
    float: left;
    padding-left: 15px;
    text-align: left;
  }

</style>
