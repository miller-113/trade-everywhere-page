<template>
  <header class="header">
    <div>
      <div class="logo">
        LOGO
      </div>
      <div>
        <ul
          v-if="menuShow || isWidthMore1150"
          class="headerUl fontWeigth500"
        >
          <li>How it works</li>
          <li>About</li>
          <li>Instructions</li>
          <li>Accounts</li>
          <li>Platforms</li>
          <li>Contact</li>
        </ul>
      </div>
    </div>
    <div>
      <div class="selectCont gray1">
        <select
          id="languages"
          class="selectLangBtn"
          name="languages"
        >
          <option value="en">
            EN
          </option>
          <option value="ua">
            UA
          </option>
        </select>
      </div>
      <ButtonComponent
        :button-styles="{ fontSize: '14px', lineHeight: '14px', padding: '13px 24px', letterSpacing: '-0.487px' }"
      >
        SIGN IN FOR FREE
      </ButtonComponent>
      <img
        class="burgerMenu displayNone"
        :src="require('@/assets/header/img/eva_menu-fill.png')"
        alt="Burger menu"
        @click="menuShow = !menuShow"
      >
    </div>
  </header>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
    name: 'AppHeader',
    components: {
        ButtonComponent,
    },
    data: () => ({
        menuShow: false,
        windowWidth: window.innerWidth,
    }),
    computed: {
        isWidthMore1150(){
            return this.windowWidth > 1150;
        }
    },
    mounted() {
        window.addEventListener('resize', this.handleResize);
    },
    methods: {
        handleResize() {
            setTimeout(() => {
                this.windowWidth = window.innerWidth;
            }, 100)

        }
    },

}
</script>

<style scoped>
    .header {
        height: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        margin: 0 57px 0 120px;
        font-size: 1.5rem;
        font-weight: 700;

    }

    .header > div:first-child {
        display: flex;
    }

    .header > div:last-child {
        margin-right: 60px;
    }

    .headerUl {
        display: flex;
        list-style: none;
        margin: 0;
        padding: 0;
        font-size: 1.5rem;
    }

    .headerUl > li {
        margin-right: 32px;
    }

    .selectLangBtn {
        border: 0;
        padding: 0 6.75px;
    }

    .selectCont {
        display: inline-block;
        margin-right: 24px;
        padding: 9.25px 12px;
        border: 1px solid rgba(0, 0, 0, 1);
        border-radius: 60px;
        line-height: 16px;
        font-size: 1.5rem;
    }

    .selectLangBtn:focus {
        outline: none;
        box-shadow: none;
    }

    @media only screen and (max-width: 1150px) {
        .selectCont, .logo, .headerUl {
            display: none;
        }

        .header > div:last-child {
            margin-right: 28px;
        }

        .burgerMenu {
            display: initial;
            margin-left: 48px;
        }

        .headerUl {
            display: flex;
            flex-direction: column;
            position: absolute;
            right: 5px;
            top: 70px;
            background-color: #ecebeb;
            border-radius: 20px;
            padding: 5px;
        }
    }

    @media only screen and (max-width: 500px) {
        .customBtn{
            display: none;
        }
        .logo {
            display: initial;
            margin: 30px 0 34px 20px;
        }

    }
</style>