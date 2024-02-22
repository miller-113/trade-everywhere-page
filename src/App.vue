<template>
  <Header/>
  <TradeEverywhere/>
  <GettingStartIsFastEasy/>
  <PeopleLoveBigInvest/>
  <FrequentlyAskedQuestion/>
  <ContactUs/>
  <AppFooter/>
</template>

<script>
import Header from './components/AppHeader.vue';
import TradeEverywhere from './components/1_sectionTradeEverywhere/AppTradeEverywhere.vue';
import GettingStartIsFastEasy from './components/2_sectionGettingStarted/AppGettingStartIsFastEasy.vue';
import PeopleLoveBigInvest from './components/3_sectionPeopleLoveBigInvest/AppPeopleLoveBigInvest.vue';
import FrequentlyAskedQuestion from './components/4_sectionFrequentlyAskedQuestions/AppFrequentlyAskedQuestion.vue';
import ContactUs from './components/5_sectionContactUs/AppContactUs.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    Header,
    TradeEverywhere,
    GettingStartIsFastEasy,
    PeopleLoveBigInvest,
    FrequentlyAskedQuestion,
    ContactUs,
    AppFooter,
  }
}
</script>
