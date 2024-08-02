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
          ID {{lottery.id}}
        </div>

        <div class="LotteriesPage_ItemLogo">
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
          }]

        //sel: null,

      };
    },

    methods:{

      getClass(lottery_name){
        if (lottery_name === 'Amethyst') {
          return 'LotteriesPage_Amethyst';
        } else if (lottery_name ==='Emerald') {
          return 'LotteriesPage_Emerald';
        } else if (lottery_name ==='Sapphire') {
          return 'LotteriesPage_Sapphire';
        } else if (lottery_name ==='Ruby') {
          return 'LotteriesPage_Ruby';
        } else if (lottery_name ==='Diamond') {
          return 'LotteriesPage_Diamond';
        } else if (lottery_name ==='Opal') {
          return 'LotteriesPage_Opal';
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
    padding: 2%;
    background: rgba(1, 9, 31, 1);
    min-height: 100vh;
  }
  .LotteriesPage_List{
    display: grid;
    grid-template-columns: repeat(auto-fit, 152px);
    justify-content: center;
    gap: 16px; /*расстояние между карточками*/
  }
  .LotteriesPage_ListItem{
    border: 2px solid rgba(255, 255, 255, 0.5);
    box-shadow: 0px 0px 16px 0px rgba(237, 89, 237, 0.9);

    /* вопрос: как лучше работать с изменением размеров карточек, текст тоже подстраивать? */
    width: 152px; /* минимальная ширина карточки */
    height: 319px; /* минимальная ширина карточки */

    padding: 10px 12px 10px 12px;
    gap: 10px;
    border-radius: 16px 16px 16px 16px;
    opacity: 0px;
  }

  .LotteriesPage_Amethyst{
    background:
      radial-gradient(circle at 100% 100%, rgba(58, 56, 153, 0.75) 0%, rgba(7, 44, 18, 0) 50%),
      radial-gradient(circle at 0% 0%, rgba(45, 62, 150, 0.75) 0%, rgba(45, 62, 150, 0) 50%),
      radial-gradient(ellipse 90% 80% at 0% 35.46%, rgba(237, 89, 237, 0.9) 0%, rgba(237, 89, 237, 0) 90%),
      radial-gradient(circle at 74.22% 22.5%, rgba(103, 32, 143, 0) 0%, rgba(103, 32, 143, 1) 100%),
      conic-gradient(from 270deg at 100% 43.7%, rgba(56, 30, 132, 0.25) 0deg, rgba(56, 30, 132, 0.5) 360deg),
      linear-gradient(175.57deg, rgba(216, 88, 229, 1) -1.54%, rgba(78, 42, 141, 1) 19.51%, rgba(36, 51, 149, 1) 82.04%, rgba(11, 5, 35, 1) 96.41%);
  }
  .LotteriesPage_Emerald{
  }
  .LotteriesPage_Sapphire{
  }
  .LotteriesPage_Ruby{
  }
  .LotteriesPage_Diamond{
  }
  .LotteriesPage_Opal{ 
  }

  .LotteriesPage_ItemID{
    font-family: sans-serif;
    font-size: 8px;
    font-weight: 400;
    text-align: right;
    color: rgba(255, 255, 255, 1);
    width: 100%;
    max-height: 10px;
  }

  .LotteriesPage_ItemLogo{
    /*background-color: black;
    border-radius: 50%;
    height: 50px;
    width: 50px;*/
  }

</style>
