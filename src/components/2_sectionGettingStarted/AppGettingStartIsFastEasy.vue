<template>
  <div class="localCont">
    <div class="customH2 marginBottom60 fontWeigth500 formH2">
      Getting Started Is <span class="purpleBackground">Fast & Easy</span>
    </div>
    <FormComponent
      digit="01."
      title="Register"
      description="Complete the simple registration to get your trading credentials."
      position-class="postion"
    />
    <VectorComponent position-class="vectorPos1" />
    <FormComponent
      digit="02."
      title="Verification"
      description="Big Invest is required to verify your identity, upload your documents quickly and get approved in minutes."
      position-class="postion2Form"
    />
    <VectorComponent position-class="vectorPos2" />
    <FormComponent
      digit="03."
      title="Deposit funds"
      description="Big Invest accepts credit cards and bank wires. Just use the secure deposit form and follow the steps."
      position-class="postion3Form"
    />
    <VectorComponent position-class="vectorPos3" />
    <FormComponent
      digit="04."
      title="Start Trading"
      description="Once your deposit has been credited, you can begin trading instantly. In no time you will see profits rolling into your account."
      position-class="postion4Form"
    />
  </div>
</template>

<script>
import FormComponent from './FormComponent.vue';
import VectorComponent from './VectorComponent.vue';

export default {
    components: {
        FormComponent,
        VectorComponent
    }
};
</script>

<style scoped>
    .localCont {
        margin: 140px 222px 140px 120px;
        height: 950px;
        display: flex;
        flex-direction: column;
    }

    .formH2{
        width: 483px;
        height: 140px;
    }

    @media only screen and (max-width: 1150px) {
        .localCont{
            margin: 120px 40px;
            height: 1029px;
        }
    }

    @media only screen and (max-width: 670px) {
        .formH2 {
            width: auto;
            height: auto;
            margin-bottom: 8px;
        }

        .localCont {
            margin: 80px 20px;
            height: auto;
            gap: 24px;
        }
    }
</style>