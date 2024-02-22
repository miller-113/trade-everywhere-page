<template>
  <div
    class="formContent"
    :class="positionClass"
  >
    <div class="innerContent">
      <div class="digit fontWeigth500">
        {{ digit }}
      </div>
      <div class="formName fontWeigth500">
        {{ title }}
      </div>
      <div class="addtitionalInfo">
        {{ description }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
    name: 'FormComponent',
    props: {
        digit: String,
        title: String,
        description: String,
        positionClass: String
    }
};
</script>

<style scoped>
    .formContent {
        border: 2px solid rgba(98, 72, 255, 1);
        border-radius: 30px;
        width: 483px;
        padding: 32px;
        z-index: 5;
        background-color: rgba(255, 255, 255, 1);
    }

    .digit {
        margin-bottom: 8px;
        color: rgba(98, 72, 255, 1);
    }

    .formName {
        margin-bottom: 24px;
        color: rgba(51, 51, 51, 1);
        font-size: 2.4rem;
    }

    .addtitionalInfo {
        font-size: 1.8rem;
        font-weight: 400;
        color: rgba(79, 79, 79, 1);
        font-family: 'Montserrat', sans-serif;
    }

    .postion2Form {
        position: absolute;
        top: 1296px;
        left: 735px;
    }

    .postion3Form {
        position: absolute;
        top: 1477px;
        left: 120px;
    }

    .postion4Form {
        position: absolute;
        top: 1657px;
        left: 735px;
    }

    @media only screen and (max-width: 1150px) {
        .formContent {
            width: 47.82%;
        }
        .postion2Form {
            align-self: end;
            position: relative;
            top: -140px;
            left: 0;
        }
        .postion3Form {
            /* align-self: end; */
            position: relative;
            top: -280px;
            left: 0;
        }
        .postion4Form {
            align-self: end;
            position: relative;
            top: -420px;
            left: 0;
        }
    }
     @media only screen and (max-width: 670px) {
        [class*="postion"] {
            position: initial;
            width: 100%;
        }
    }
</style>