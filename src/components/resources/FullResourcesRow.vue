<template>
  <div class="row" style="padding-top: 10px">
    <div :class="'col-sm-' + ((12 - resourcesAmount) / 2)"></div>
    <resources-item v-for="resource in resources"
      :res="resource"
    />
  </div>
</template>

<script>
  import ResourcesItem from "./ResourcesItem.vue";

  export default {
    props: ['resources', 'resourcesAmount'],
    components: {
      ResourcesItem
    }
  }
</script>
