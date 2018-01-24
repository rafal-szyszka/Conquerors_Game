<template>
  <div>
    <full-resources-table v-if="fullList"/>
    <div class="container" @click="toggleListView">
      <div class="row gradient-bg">
        <div class="col-sm-12" style='color: white; text-align: center'>
          <i class="fa" :class="toggleList"></i>
        </div>
      </div>
      <main-resources-row :resources-items="mainResources" :show-split="true" class="cnq-resources-row gradient-bg"/>
    </div>
  </div>
</template>

<script>
  import MainResourcesRow from './MainResourcesRow.vue';
  import FullResourcesTable from "./FullResourcesTable.vue";

  export default {
    data: function () {
      return {
        fullList: false,
        trigger: 'trigger',
        toggleButtonClass: 'fa-chevron',
        toggleList: 'fa-chevron-down',
        mainResources: [
          {
            name: "Ludzie", imgSource: "./src/assets/resources-icons/res-workers.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Armia", imgSource: "./src/assets/resources-icons/res-army.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Drewno", imgSource: "./src/assets/resources-icons/res-wood.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Kamień", imgSource: "./src/assets/resources-icons/res-stone.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Narzędzia", imgSource: "./src/assets/resources-icons/res-tools.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Glina", imgSource: "./src/assets/resources-icons/res-brick.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Jedzenie", imgSource: "./src/assets/resources-icons/res-food.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Złoto", imgSource: "./src/assets/resources-icons/res-gold.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Diamenty", imgSource: "./src/assets/resources-icons/res-diamond.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
          {
            name: "Coinquers", imgSource: "./src/assets/resources-icons/res-coinquers.png",
            amount: Math.floor((Math.random() * 99999) + 1)
          },
        ],
      }
    },
    methods: {
      toggleListView: function () {
        const downArrow = this.toggleButtonClass + '-down',
          upArrow = this.toggleButtonClass + '-up';

        this.toggleList = this.toggleList === downArrow ? upArrow : downArrow;
        this.fullList = !this.fullList;
        this.trigger = this.toggleList;
      },

      beforeEnter: function (el) {
        console.log("beforeEnter");
      }
    },
    components: {
      FullResourcesTable,
      MainResourcesRow
    }
  }

</script>

<style>

  .gradient-bg {
    background: rgba(50, 50, 50, 1);
    background: -moz-linear-gradient(left, rgba(41, 41, 41, 1) 0%, rgba(65, 65, 65, 1) 50%, rgba(41, 41, 41, 1) 100%);
    background: -webkit-gradient(left top, right top, color-stop(0%, rgba(21, 21, 21, 1)), color-stop(50%, rgba(45, 45, 45, 1)), color-stop(100%, rgba(21, 21, 21, 1)));
    background: -webkit-linear-gradient(left, rgba(41, 41, 41, 1) 0%, rgba(65, 65, 65, 1) 50%, rgba(41, 41, 41, 1) 100%);
    background: -o-linear-gradient(left, rgba(41, 41, 41, 1) 0%, rgba(65, 65, 65, 1) 50%, rgba(41, 41, 41, 1) 100%);
    background: -ms-linear-gradient(left, rgba(41, 41, 41, 1) 0%, rgba(65, 65, 65, 1) 50%, rgba(41, 41, 41, 1) 100%);
    background: linear-gradient(to right, rgba(41, 41, 41, 1) 0%, rgba(65, 65, 65, 1) 50%, rgba(41, 41, 41, 1) 100%);
  }

  @import url('https://fonts.googleapis.com/css?family=Quicksand');

  .cnq-resources-row {
    border-bottom-right-radius: 40px;
    border-bottom-left-radius: 40px;
    color: aliceblue;
    font-family: 'Quicksand', sans-serif;
    padding-top: 10px;
  }

  .slide-enter-active {
    animation: slide-in 750ms ease-in-out forwards;
  }

  .slide-leave-active {
    animation: slide-out 750ms ease-in-out forwards;
  }

  @keyframes slide-in {
    from {
      transform: translateY(-248px);
    }
    to {
      transform: translateY(0px);
    }
  }

  @keyframes slide-out {
    from {
      transform: translateY(0px);
    }
    to {
      transform: translateY(-248px);
    }
  }

</style>
