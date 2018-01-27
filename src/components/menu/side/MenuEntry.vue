<template>
  <div class="row">
    <div class="col-sm-2 cnq-menu-entry" v-if="menuElement.isModalDialog">
      <button class="btn btn-menu-entry">
        <img :src="menuElement.imgSrc"/>
        {{ menuElement.name }}
      </button>
    </div>
    <div class="col-sm-2 cnq-menu-entry last-entry" v-else>
      <button class="btn btn-menu-entry">
        <img :src="menuElement.imgSrc"/>
        {{ menuElement.name }}
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    name: "menu-entry",
    props: ['menuElement', 'totalElements', 'currentElement']
  }
</script>

<style scoped>

  @import url('https://fonts.googleapis.com/css?family=Quicksand');

  .btn-menu-entry {
    background-color: #754237;
    border: 1px solid saddlebrown;
    color: whitesmoke;
    font-family: "Quicksand", sans-serif;
    font-weight: 600;
    width: inherit;
  }

  .cnq-menu-entry {
    background-color: burlywood;
    border-top: 1px solid black;
    padding: 15px 10px 15px 15px;
    text-align: center;
  }

  .last-entry {
    background-color: burlywood;
    border-top: 1px solid black;
    border-bottom-right-radius: 15px;
    padding: 15px 10px 15px 15px;
    text-align: center;

  }

</style>
