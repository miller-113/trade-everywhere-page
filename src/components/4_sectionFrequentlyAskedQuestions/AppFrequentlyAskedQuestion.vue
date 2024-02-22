<template>
  <div class="localContent">
    <div class="customH2 fontWeigth500 formH2">
      Frequently asked <span class="purpleBackground">questions</span>
    </div>
    <div class="formsContent">
      <FormFaq
        v-for="item, index in formsData"
        :key="index"
        :title="item.title"
        :additional-text="item.additionalText"
        :active="item.active"
        @onActive="changeActive($event, index)"
      />
    </div>
  </div>
</template>

<script>
import FormFaq from './FormFaq.vue';
export default {
    name: 'FrequentlyAskedQuestion',
    components: {
        FormFaq,
    },
    data: () => ({
        formsData: [
            {
                title: "How do I change my details?",
                additionalText:"We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!",
            },
            {title: "What platforms will I be able to use?"},
            {title: "How do I change my details?"},
            {title: "How do I change my details?"},
            {title: "How do I change my details?"},
            {title: "How do I change my details?"},
            {title: "How do I change my details?"},

        ]
    }),
    methods: {
        changeActive(val, index){
            this.formsData.forEach((item, idx) => {
                if (idx !== index) {
                    item.active = false;
                }
            });
            this.formsData[index].active = val
        }
    }
}
</script>

<style scoped>
    .formsContent {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        margin-top: 60px;
        gap: 16px;
    }

    .formH2 {
        width: 483px;
        height: 140px;
    }
    .localContent {
        margin: 0 223px 140px 120px;
        padding-top: 30px;
    }

    @media only screen and (max-width: 1150px) {
        .localContent {
            padding: 0;
            margin: 0 40px 120px;
        }

        .form {
            width: 100%;
        }

        .formsContent {
            margin-top: 48px;
        }
    }

    @media only screen and (max-width: 670px) {
        .formH2 {
            width: auto;
            height: auto;
            margin-bottom: 8px;
        }

        .localContent {
            margin: 0 20px 80px;
            height: auto;
            gap: 24px;
        }

        .form {
            font-size: 1.8rem;
            line-height: 21.6px;
            padding: 24px 16px;
        }

        .formsContent {
            margin-top: 32px;
        }
    }
</style>