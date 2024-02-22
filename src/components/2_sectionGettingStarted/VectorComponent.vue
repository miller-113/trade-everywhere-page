<template>
    <div class="vector-container" :class="positionClass">
        <img :src="require('@/assets/gettingStartIsFastEasy/Vector 34.png')" alt="Growing Graphs">
    </div>
</template>

<script>
export default {
    name: 'VectorComponent',
    props: {
        positionClass: String
    }
};
</script>

<style scoped>
    .vector-container {
        position: absolute;
        z-index: 1;
    }

    .vectorPos1 {
        top: 1227px;
        left: 603px;
    }

    .vectorPos2{
        top: 1407px;
        left:736px;
        transform: scaleX(-1);
        transform-origin: left center;
    }

    .vectorPos3 {
        top: 1588px;
        left: 603px;

    }

    @media only screen and (max-width: 1150px) {
        .vector-container {
            position: relative;
            z-index: 1;
            width: fit-content;
       }

        .vectorPos1 {
            top: -120px;
            left: 350px;
        }

        .vectorPos2{
            top: -265px;
            left: 585px;
            transform: scaleX(-1);
            transform-origin: left center;
        }

        .vectorPos3 {
            top: -405px;
            left: 350px;
        }
    }
    @media only screen and (max-width: 900px) {

        .vectorPos1 {
            left: 140px;
        }

        .vectorPos2{
            left: 535px;
        }

        .vectorPos3 {
            left: 140px;
        }
    }

    @media only screen and (max-width: 670px) {
        .vector-container {
            display: none;
        }
    }
</style>