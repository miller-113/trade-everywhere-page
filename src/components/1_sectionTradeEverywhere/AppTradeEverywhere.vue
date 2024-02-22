<template>
  <div class="content">
    <div class="info">
      <div class="h1Custom fontWeigth500">
        <div>Trade everywhere.</div>
        <div>Invest here!</div>
      </div>
      <div class="additionalInfo">
        We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere.
      </div>
      <div>
        <ButtonComponent>START TRADING</ButtonComponent>
      </div>
    </div>
    <div class="imgCont">
      <img
        :src="require('@/assets/tradeEverywhere/growingGraphs.png')"
        alt="Growing Graphs"
      >
    </div>
  </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'TradeEverywhere',
    components: {
        ButtonComponent
    }
}
</script>

<style scoped>

    .info {
        height: 398px;
        width: 585px;
    }
    .content {
        height: 720px;
        background-color: rgb(98 72 255 / 10%);
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        flex-wrap: wrap;
    }

    .h1Custom {
        font-size: 6.4rem;
        line-height: 7.2rem;
    }

    .additionalInfo {
        margin: 32px 0 48px 0;
        width: 483px;
        height: 120px;
        color: #4F4F4F;
        font-family: 'Montserrat', sans-serif;
        font-size: 18px;
        font-weight: 400;
        line-height: 30px;
        letter-spacing: 0em;
        text-align: left;
    }

    @media only screen and (max-width: 1150px) {
        .content {
            justify-content: center;
            text-align: center;
            height: auto;
        }

        .h1Custom {
            margin-top: 40px;
        }

        .info {
            height: auto;
        }

        .additionalInfo {
            height: auto;
            width: auto;
            margin: 32px 40px 48px;
            text-align: center;
        }

        .imgCont > img {
            width: 418px;
            height: 450px;
        }

        .imgCont {
            margin: 32px 0 24px;
        }
    }

    @media only screen and (max-width: 670px) {
        .h1Custom {
            font-size: 4rem;
            line-height: 44px;
            margin: 0;
        }

        .content {
            text-align: start;
            padding: 32px 20px 16px;
        }

        .additionalInfo {
            margin: 24px 0 0;
            text-align: inherit;
        }

        .customBtn {
            width: 100%;
            margin-top: 32px;
        }

        .imgCont, .imgCont > img {
            width: 100%;
            height: auto;
        }
    }
</style>