<template>
  <div class="container" @click="toggleListView">
    <full-resources-row class="gradient-bg" style="color: white"
      v-for="resourceGroup in allResources"
      :resources="resourceGroup"
      :resources-amount="resourceGroup.length"
    />
  </div>
</template>

<script>
  import FullResourcesRow from "./FullResourcesRow.vue";

  export default {
    data: function () {
      return {
        allResources: [
          [
            {
              name: "Miedź", imgSource: "./src/assets/resources-icons/res-copper.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Żelazo", imgSource: "./src/assets/resources-icons/res-iron.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Węgiel", imgSource: "./src/assets/resources-icons/res-coal.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Stal", imgSource: "./src/assets/resources-icons/res-steel.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            }
          ],
          [
            {
              name: "Mięso", imgSource: "./src/assets/resources-icons/res-meat.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Owoce", imgSource: "./src/assets/resources-icons/res-fruit.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Nabiał", imgSource: "./src/assets/resources-icons/res-dairy.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Pszenica", imgSource: "./src/assets/resources-icons/res-wheat.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Mąka", imgSource: "./src/assets/resources-icons/res-flour.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Chleb", imgSource: "./src/assets/resources-icons/res-bread.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            }
          ],
          [
            {
              name: "Wełna", imgSource: "./src/assets/resources-icons/res-wool.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Bawełna", imgSource: "./src/assets/resources-icons/res-cotton.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Skóra", imgSource: "./src/assets/resources-icons/res-leather.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Ubrania", imgSource: "./src/assets/resources-icons/res-coats.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            }
          ],
          [
            {
              name: "Srebro", imgSource: "./src/assets/resources-icons/res-silver.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Platyna", imgSource: "./src/assets/resources-icons/res-platinum.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Broń strzelecka", imgSource: "./src/assets/resources-icons/res-rifles.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Artyleria", imgSource: "./src/assets/resources-icons/res-cannons.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Amunicja", imgSource: "./src/assets/resources-icons/res-rifle-ammo.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            },
            {
              name: "Amunicja artyleryjska", imgSource: "./src/assets/resources-icons/res-cannon-ammo.png",
              amount: Math.floor((Math.random() * 99999) + 1)
            }
          ]
        ]
      }
    },
    components: {
      FullResourcesRow,
    }
  }
</script>
