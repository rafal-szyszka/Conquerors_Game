<template>
  <div id="cnq-resources-table">
    <cnq-resources-row
      v-for="resourceItem in resources"
      :resourcesItems="resourceItem.resources"
      :resourcesType="resourceItem.type"
      :showSplit="resourceItem.showSplit"
    />
  </div>
</template>

<script>
  import ResourcesRow from './ResourcesRow.vue';

  export default {
    data: function () {
      return {
        resources: [
          {
            type: "Materiały budowlane",
            resources:
              [
                {name: "Drewno", imgSource: "./src/assets/resources-icons/res-wood.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Kamień", imgSource: "./src/assets/resources-icons/res-stone.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Żelazo", imgSource: "./src/assets/resources-icons/res-iron.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Glina", imgSource: "./src/assets/resources-icons/res-brick.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Stal", imgSource: "./src/assets/resources-icons/res-steel.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
              ]
          },
          {
            resources:
              [
                {name: "Narzędzia", imgSource: "./src/assets/resources-icons/res-tools.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Węgiel", imgSource: "./src/assets/resources-icons/res-coal.png",
                  amount: Math.floor((Math.random() * 99999) + 1)}
              ]
          },
          {
            type: "Żywność",
            showSplit: true,
            resources:
              [
                {name: "Mięso", imgSource: "./src/assets/resources-icons/res-meat.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Chleb", imgSource: "./src/assets/resources-icons/res-bread.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Owoce", imgSource: "./src/assets/resources-icons/res-fruit.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Nabiał", imgSource: "./src/assets/resources-icons/res-dairy.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Pszenica", imgSource: "./src/assets/resources-icons/res-wheat.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
              ]
          },
          {
            resources:
              [
                {name: "Mąka", imgSource: "./src/assets/resources-icons/res-flour.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
              ]
          },
          {
            type: "Pozostałe",
            showSplit: true,
            resources:
              [
                {name: "Ubrania", imgSource: "./src/assets/resources-icons/res-coats.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Wełna", imgSource: "./src/assets/resources-icons/res-wool.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Bawełna", imgSource: "./src/assets/resources-icons/res-cotton.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Skóra", imgSource: "./src/assets/resources-icons/res-leather.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
              ]
          },
          {
            type: "Luksusowe",
            showSplit: true,
            resources:
              [
                {name: "Srebro", imgSource: "./src/assets/resources-icons/res-silver.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Złoto", imgSource: "./src/assets/resources-icons/res-gold.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Diamenty", imgSource: "./src/assets/resources-icons/res-diamond.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
                {name: "Coinquers", imgSource: "./src/assets/resources-icons/res-coinquers.png",
                  amount: Math.floor((Math.random() * 99999) + 1)},
              ]
          }
        ]
      }
    },
    components: {
      'cnq-resources-row': ResourcesRow
    }
  }

</script>

<style>
  #cnq-resources-table {
    background-color: rgba(23, 12, 29, 0.8);
    border: 2px solid rgba(13, 2, 19, 0.8);
    border-bottom-width: 5px;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    border-top-width: 0px;
    color: white;
    display: table;
    margin: auto;
    font-family: sans-serif;
  }
</style>
