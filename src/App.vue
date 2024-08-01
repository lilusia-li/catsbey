<template>
  <div class="LotteriesPage">
    <div class="LotteriesPage_List">
      <div 
        v-for="lottery in lotteries" 
        v-bind:key="lottery.name"
        v-bind:class="getClass(lottery.name)"
        class="LotteriesPage_ListItem"
      >
        <div class="LotteriesPage_ItemID">
          fdgs
        </div>

        <div class="LotteriesPage_ItemLogo">
          dsf
        </div>

        <div class="LotteriesPage_ItemName">
        
        </div>

        <div class="LotteriesPage_ItemPrice">
        
        </div>
        
        <div class="LotteriesPage_ItemStatistic">
        
        </div>
        
        <div class="LotteriesPage_ItemTime">
        
        </div>
        
        <div class="LotteriesPage_ItemPurchaseButton">
        
        </div>
        
      </div>
      
    </div>

  </div>

  <!--
    v-on:click="sel=cours"
    v-bind:class="{
      'selected-border': sel == cours
    }"
  -->
</template>

<script>
  export default {
    name: 'App',
    data(){
      return{
        lotteries: [
          {
            "id": "23094587",
            "name": "Amethyst",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Emerald",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Emerald",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Emerald",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          }
        ],

        //sel: null,

      };
    },

    methods:{

      getClass(lottery_name){
        if (lottery_name === 'Amethyst') {
          return 'LotteriesPage_Amethyst';
        } else if (lottery_name ==='Emerald') {
          return 'LotteriesPage_Emerald';
        }
      },

    }

  }
</script>

<style>
  * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
  }

  .LotteriesPage{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 2%;
    background: rgba(1, 9, 31, 1);
    height: 100vh;
  }
  .LotteriesPage_List{
    display: flex;
    flex-wrap: wrap; /*то, что не влезло в строку, переносится на следующую*/
    justify-content: flex-start; /*центрирование по горизонтали*/
    align-items: center; /*центрирование по вертикали*/
    gap: 16px; /*расстояние между карточками*/
  }
  .LotteriesPage_ListItem{
    border: 2px solid rgba(255, 255, 255, 0.5);
    box-shadow: 0px 0px 16px 0px rgba(237, 89, 237, 0.9);

    /* вопрос: как лучше работать с изменением размеров карточек, текст тоже подстраивать? */
    min-width: 152px; /* минимальная ширина карточки */
    min-height: 319px; /* минимальная ширина карточки */

    padding: 12px 0px 12px 0px;
    gap: 10px;
    border-radius: 16px 0px 0px 0px;
    opacity: 0px;


  }
  
  
  


  .LotteriesPage_Amethyst{
    background:
      linear-gradient(175.57deg, #D858E5 -1.54%, #4E2A8D 19.51%, #243395 82.04%, #0B0523 96.41%),
      conic-gradient(from 270deg at 100% 43.7%, rgba(56, 30, 132, 0) 0deg, #381E84 360deg),
      radial-gradient(circle at 74.22% 22.5%, rgba(103, 32, 143, 0) 0%, #67208F 100%),
      radial-gradient(circle at 0% 41.46%, rgba(237, 89, 237, 0.75) 0%, rgba(237, 89, 237, 0) 100%),
      radial-gradient(circle at 0% 0%, rgba(45, 62, 150, 0.75) 0%, rgba(45, 62, 150, 0) 100%),
      radial-gradient(circle at 100% 100%, rgba(58, 56, 153, 0.75) 0%, rgba(7, 44, 18, 0) 100%);
  }
  .LotteriesPage_Emerald{
    background:
      linear-gradient(175.57deg, #D858E5 -1.54%, #4E2A8D 19.51%, #243395 82.04%, #0B0523 96.41%),
      conic-gradient(from 270deg at 100% 43.7%, rgba(56, 30, 132, 0) 0deg, #381E84 360deg),
      radial-gradient(circle at 74.22% 22.5%, rgba(103, 32, 143, 0) 0%, #67208F 100%),
      radial-gradient(circle at 0% 41.46%, rgba(237, 89, 237, 0.75) 0%, rgba(237, 89, 237, 0) 100%),
      radial-gradient(circle at 0% 0%, rgba(45, 62, 150, 0.75) 0%, rgba(45, 62, 150, 0) 100%),
      radial-gradient(circle at 100% 100%, rgba(58, 56, 153, 0.75) 0%, rgba(7, 44, 18, 0) 100%);
  }

  .LotteriesPage_ItemID{}

</style>
