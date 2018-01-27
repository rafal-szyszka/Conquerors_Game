<template>
  <div class="container-fluid" style="position: absolute; top: 90px; z-index: -1;">
    <div class="row">
      <div class="col-sm-2 cnq-menu-bar">
        <img src="../../../assets/cnqrrs.png" width="200px"/>
      </div>
    </div>
    <menu-entry
      v-for="menuEntry in menuEntries"
      :menu-element="menuEntry"
    />
  </div>
</template>

<script>
  import MenuEntry from "./MenuEntry";

  export default {
    components: {MenuEntry},
    name: "main-side-menu",
    data: function () {
      return {
        menuEntries: [
          {name: "Zadania", isModalDialog: true, imgSrc: "./src/assets/menu-icons/menu-tasks.png"},
          {name: "Depesze", isModalDialog: true, imgSrc: "./src/assets/menu-icons/menu-reports.png"},
          {name: "Wiadomości", isModalDialog: true, imgSrc: "./src/assets/menu-icons/menu-messages.png"},
          {name: "Ranking", isModalDialog: true, imgSrc: "./src/assets/menu-icons/menu-rank.png"},
          {name: "Pomoc", isModalDialog: true, imgSrc: "./src/assets/menu-icons/menu-help.png"},
          {name: "Wyloguj", isModalDialog: false}
        ]
      }
    }
  }
</script>

<style scoped>

  .cnq-menu-bar {
    background-color: burlywood;
    border-top-right-radius: 75px;
    padding: 10px 10px 20px 20px;
  }

</style>
