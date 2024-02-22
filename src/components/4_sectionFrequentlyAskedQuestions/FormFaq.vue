<template>
  <div class="form">
    <div class="openCloseCont">
      <div class="title fontWeigth500">
        {{ title }}
      </div>
      <div
        class="openClose"
        @click="turnActive"
      >
        <span v-if="!active">
          <img
            :src="require('@/assets/faq/bi_plus.png')"
            alt="Growing Graphs"
          >
        </span>
        <span v-else>
          <img
            :src="require('@/assets/faq/bi_plusclose.png')"
            alt="Growing Graphs"
          >
        </span>
      </div>
    </div>
    <transition name="fade">
      <div
        v-show="active"
        class="additionalText"
      >
        {{ additionalText }}
      </div>
    </transition>
  </div>
</template>

<script scoped>
export default {
    props: {
        title: {required: true, type: String},
        additionalText: {type: String, default: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus repellat nemo praesentium eum non illo, dicta molestias culpa deleniti facere consequuntur explicabo, debitis iusto, aliquid fugiat recusandae reiciendis voluptatem quod.'},
        active: {default: false, type: Boolean}
    },
    methods:{
        turnActive(){
            this.$emit('onActive', !this.active);
        }
    }
}
</script>

<style scoped>
    .title {
        font-size: 2.4rem;
        line-height: 28.8px;
        color: rgba(51, 51, 51, 1);
    }

	.fade-enter-active{
		animation: fadeIn 1.5s;
	}

	.fade-leave-active{
		animation: fadeOut 1.5s;
	}

	@keyframes fadeIn {
		from{ opacity: 0; transform: translateY(-100px); }
		to{ opacity: 1; transform: translateY(0);}
	}

	@keyframes fadeOut {
		from{ opacity: 1; transform: translateY(0); }
		to{ opacity: 0; transform: translateY(100px); }
	}

    .additionalText {
        margin-top: 24px;
        font-family: 'Montserrat', sans-serif;
        font-weight: 400;
        font-size: 1.6rem;
        line-height: 27px;
    }

    .form {
        border: 2px solid rgba(98, 72, 255, 1);
        background-color: rgba(255, 255, 255, 1);
        width: 995px;
        border-radius: 20px;
        padding: 33.5px 32px 33.5px 40px;
    }
    .openCloseCont {
        display: flex;
        justify-content: space-between;
    }

    @media only screen and (max-width: 670px) {
        .openCloseCont {
            align-items: center;
        }
    }
</style>