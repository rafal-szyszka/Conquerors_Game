<template>
  <div class="cnq-resources-table-row">
    <hr v-if="showSplit">
    <p v-if="resourcesType !== undefined" class="cnq-resources-type-label">{{ resourcesType }}</p>
    <table v-if="resourcesType !== undefined" style="margin-top: -15px">
      <tr>
        <cnq-resource-item
          v-for="resource in resourcesItems"
          :name="resource.name"
          :amount="resource.amount"
          :imgSource="resource.imgSource"
        />
      </tr>
    </table>
    <table v-else style="margin-bottom: -10px; margin-top: -5px">
      <tr>
        <cnq-resource-item
          v-for="resource in resourcesItems"
          :name="resource.name"
          :amount="resource.amount"
          :imgSource="resource.imgSource"
        />
      </tr>
    </table>
  </div>
</template>

<script>
  import ResourcesItem from './ResourcesItem.vue';

  export default {
    props: ['showSplit', 'resourcesType', 'resourcesItems'],
    components: {
      'cnq-resource-item': ResourcesItem
    }
  }

</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Quicksand');

  .cnq-resources-type-label {
    font-family: 'Quicksand', sans-serif;
    font-size: 22px;
  }

  .cnq-resources-table-row {
    display: table;
    margin: 0 auto;
    text-align: center;
    padding-left: 10px;
    padding-right: 10px;
    width: inherit;
  }

</style>
