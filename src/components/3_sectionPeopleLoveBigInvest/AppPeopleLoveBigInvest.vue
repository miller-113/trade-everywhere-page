<template>
    <div class="localContent">
        <div>
            <div class="customH2 fontWeigth500 formH2">
                People love <span class="purple320">Big<span class="purpleBackground"> Invest</span></span>
            </div>

            <div class="btnsCont">
                <ButtonComponent
                :class="['circleBtn', 'inactiveBtn']"
                :style="{ padding: '0'}"
                :disabled="true"
                >
                    <img :src="require('@/assets/peopleLoveBigInvest/entypo_chevron-small-down left.png')" alt="Growing Graphs">
                </ButtonComponent>

                <ButtonComponent
                :class="['circleBtn']"
                :style="{padding: '0'}"
                >
                    <img :src="require('@/assets/peopleLoveBigInvest/entypo_chevron-small-down right.png')" alt="Growing Graphs">
                </ButtonComponent>

            </div>
        </div>

        <div>
            <div class="person">
                <div class="personImg">
                    <img :src="require('@/assets/peopleLoveBigInvest/Alberto Abello.png')" alt="Growing Graphs">
                </div>
                <div class="presonInfo">
                    <div class="personName fontWeigth500">Albert Abello</div>
                    <div class="personPosition">Director of Growth</div>
                </div>
            </div>
            <div class="info fontWeigth500">
                This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.
            </div>
            <div class="pages fontWeigth500">01 <span>/ 04</span></div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '/src/components/ButtonComponent.vue';

export default {
    name: "PeopleLoveBigInvest",
    components: {
        ButtonComponent
    },
}
</script>

<style scoped>
    .circleBtn {
        border: 1px solid rgba(98, 72, 255, 1);
        border-radius: 60px;
        background-color: rgba(255, 255, 255, 1) !important;
        width: 48px;
        height: 48px;
    }

    .localContent {
        display: flex;
        margin: 0 120px 140px;
        justify-content: space-between;
    }

    .localContent > div:last-child {
        width: 585px;
        margin-top: 27px;
    }

    .btnsCont {
        margin-top: 39px;
    }

    .btnsCont > button:first-child {
        margin-right: 16px;
    }

    .inactiveBtn {
        border-color: rgba(224, 224, 224, 1) !important;
    }

    .loclaContent {
        height: 282px;
        margin: 0 120px;
    }

    .formH2 {
        width: 483px;
        height: 132px;
    }

    .personName {
        font-size: 1.8rem;
        line-height: 30px;
    }

    .person {
        display: flex;
        justify-content: flex-start;
        align-items: center;
    }

    .personPosition {
        font-family: 'Montserrat', sans-serif;
        font-weight: 400;
        font-size: 1.6rem;
        line-height: 27px;
        color: rgba(79, 79, 79, 1);
    }

    .personImg {
        margin-right: 30px;
    }

    .info {
        color: rgba(51, 51, 51, 1);
        font-size: 2.4rem;
        line-height: 28.8px;
        margin-top: 17px;
        position: relative;
    }

    .info::before{
        content: url('@/assets/peopleLoveBigInvest/”.png');
        margin-right: 15px;
        position: absolute;
        top: 0;
        left: -50px;
    }

    .pages {
        margin-top: 31px;
        color: rgba(98, 72, 255, 1);
        font-size: 1.5rem;
        line-height: 18px;
    }

    .pages > span {
        color: rgba(79, 98, 246, 1);
    }

    @media only screen and (max-width: 1150px) {
        .localContent {
            display: flex;
            margin: 0 40px 120px;
            flex-direction: column;
        }

        .localContent > div:last-child {
            width: 73.838%;
            margin: 48px auto 0;
        }

        .person {
            flex-direction: column;
            margin-bottom: 55px;
        }

        .info {
            text-align: center;
        }

        .info::before {
            left: 46.5%;
            top: -42px;
        }

        .personImg {
            margin-right: 0;
        }

        .presonInfo {
            text-align: center;
        }

        .btnsCont > button:last-child {
            padding: 0px;
            position: absolute;
            right: 40px;
            border-color: rgba(224, 224, 224, 1) !important;
         }

        .btnsCont > button:first-child {
            padding: 0px;
            position: absolute;
            left: 40px;
        }

        .btnsCont {
            height: 0;
            margin: 0;
            transform: translateY(185px);
        }

        .pages {
            text-align: center;
            margin-top: 32px;
        }
    }

    @media only screen and (max-width: 670px) {
        .formH2 {
            /* width: auto; */
            height: auto;
            width: 265px;
        }

        .purple320 {
            background-color: rgb(98 72 255 / 10%);
        }

        .purpleBackground {
            background-color: unset;
        }

        .localContent {
            margin: 0 20px 80px 20px;
        }

        .localContent > div:last-child {
            margin: 32px 0 0;
            width: 100%;
        }

        .info {
            margin-top: 67px;
        }

        .info::before {
            left: 44.5%;
            top: -47px;
        }

        .localContent {
            position: relative;
        }

        .btnsCont {
            transform: none;
        }

        .btnsCont > button:first-child {
            left: 0;
            bottom: -13px;
        }

        .btnsCont > button:last-child {
            right: 0;
            bottom: -13px;
        }
    }
</style>