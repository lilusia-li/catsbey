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
          <!--<img :src="`/logos/${lottery.name}.png`" alt="Lottery Logo">-->
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
            "name": "Sapphire",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Ruby",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Diamond",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          },
          {
            "id": "23094587",
            "name": "Opal",
            "price": "500",
            "my_tickets": "1000",
            "tickets_left": "100111900",
            "time": "default"
          }],
        lotteryName: "default",

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
      getLogoSrc(lottery_name) {
        this.lotteryName = lottery_name;
        return '/logos/${lottery_name}.png';
        
      }

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
    background-image: url('@/assets/amethyst_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом*/
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
  }
  .LotteriesPage_Emerald{
    background-image: url('@/assets/emerald_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом */
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
  }
  .LotteriesPage_Sapphire{
    background-image: url('@/assets/sapphire_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом*/
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
  }
  .LotteriesPage_Ruby{
    background-image: url('@/assets/ruby_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом*/
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
  }
  .LotteriesPage_Diamond{
    background-image: url('@/assets/diamond_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом*/
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
  }
  .LotteriesPage_Opal{ 
    background-image: url('@/assets/opal_gradient.svg');
    background-size: calc(100% + 4px) calc(100% + 4px); /* Сделает изображение фоном на весь div с запасом*/
    background-position: center; /* Центрирует изображение */
    background-repeat: no-repeat; /* Предотвращает повторение изображения */
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
    width: 50px;
    /*background-color: black;
    border-radius: 50%;
    height: 50px;
    width: 50px;*/
  }

</style>
