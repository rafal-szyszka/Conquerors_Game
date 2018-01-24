<template>
  <div class="row">
    <div class="col-sm-1"></div>
    <resources-item
      v-for="(resource, index) in resourcesItems"
      :res="resource"
      :showSplit="showSplit ? index === 1 ? true : index === 8 : false"
    />
  </div>
</template>

<script>
  import ResourcesItem from './ResourcesItem.vue';

  export default {
    props: ['showSplit', 'resourcesItems'],
    components: {
      ResourcesItem
    }
  }

</script>
