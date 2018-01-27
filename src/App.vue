<template>
  <div>
    <main-resources-label />
    <main-side-menu />
  </div>
</template>

<script>
  import MainResourcesLabel from "./components/resources/MainResourcesLabel";
  import MainSideMenu from "./components/menu/side/MainSideMenu";

  export default {
    components: {
      MainSideMenu,
      MainResourcesLabel

    }
  }
</script>

<style>

</style>
