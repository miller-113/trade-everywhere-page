<template>
  <div class="content purpleBackground">
    <div class="infoPlace">
      <div class="customH2 fontWeigth500 formH2 gray1 fontMuseoSans">
        Contact us!
      </div>
      <div class="supportStaffText gray2 fontMontserrat fontWeigth400">
        The support staff and customer service are available to help you with any questions or needs you might have. Just drop us a line.
      </div>

      <div class="contactInfoCont fontWeigth400 gray2 fontMontserrat">
        This site is owned and operated by Kode Tech Solutions LTD
        <div class="contactInfo">
          <div class="phone">
            <div class="gray1 fontMuseoSans">
              Phone:
            </div>
            <div>
              <a href="tel:+442038857261">
                442038857261
              </a>
            </div>
          </div>
          <div class="email">
            <div class="gray1 fontMuseoSans">
              Email:
            </div>
            <div>
              <a href="mailto:help@google.com">
                help@google.com
              </a>
            </div>
          </div>
          <div class="address">
            <div class="gray1 fontMuseoSans">
              Address:
            </div>
            <div>
              <a href="https://www.google.com/maps?q=Trust+Company+Complex,+Ajeltake+Road,+Ajeltake+Island,+Majuro,+Republic+of+the+Marshall+Islands,+MH+96960">
                Trust Company Complex, Ajeltake Road, Ajeltake Island, Majuro, Republic of the Marshall Islands, MH 96960
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="formPlace fontWeigth400 fontMontserrat">
      <div
        v-for="field, ind in info"
        :key="ind"
        class="filedCont"
      >
        <input
          :id="field.label"
          :name="field.label"
          :value="field.value"
          :style="validStyle(field)"
          type="text"
          class="customInput"
          @input="onInput(ind, $event.target.value)"
        >
        <div
          v-if="field.activated && !field.valid"
          class="helpText"
        >
          {{ field.helpText }}
        </div>
      </div>
      <textarea
        id="message"
        class="customInput"
        name="message"
        value="Message"
        cols="30"
        rows="10"
      >Message</textarea>
      <ButtonComponent
        :style="{marginTop: '40px', letterSpacing: '-0.114px'}"
      >
        SEND
      </ButtonComponent>
    </div>
  </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: "ContactUs",
    components: {
        ButtonComponent,
    },
    data() {
        return {
            info: [
                {
                    label: 'name',
                    value: 'Name',
                    pattern: /^[a-zA-Z ]{2,30}$/,
                    helpText: 'Incorrect name type'
                },
                {
                    label: 'email',
                    value: 'Email',
                    pattern: /^[^\s@]+@[^\s@]+\.[^\s@]+$/,
                    helpText: 'Incorrect email type'
                },
            ],
        };
    },
    computed: {

    },
    created() {
        this.info.forEach(field => {
            field.valid = false;
            field.activated = false;
        })
    },
    methods: {
        onInput(i, val) {
            let field = this.info[i];
            field.value = val.trim();
            field.activated = true;
            field.valid = field.pattern.test(field.value);
        },
        validStyle(field) {
            if (!field.activated) {
                return
            }
            return field.valid ? { border: '1px solid rgba(14, 172, 0, 1)' } : {border: '1px solid rgba(235, 87, 87, 1)'}
        }
    },
}
</script>

<style scoped>
    .filedCont {
        position: relative;
    }

    .helpText {
        font-size: 1.5rem;
        font-weight: 500;
        text-align: left;
        color: rgba(235, 87, 87, 1);
        position: absolute;
        bottom: 0px;
    }

    .sendBtn {
        margin-top: 40px;
    }

    .customInput {
        border-radius: 3px;
        border: 1px solid rgba(224, 224, 224, 1);
        height: 40px;
        width: 425px;
        font-size: 1.6rem;
        line-height: 26px;
        padding: 7px 16px;
        color: rgba(130, 130, 130, 1);
    }

    .customInput:focus {
        outline-color: rgba(130, 130, 130, 1);
        border: 1px solid rgba(130, 130, 130, 1);
    }

    #name, #email {
        margin-bottom: 24px;
    }

    #message {
        resize: none;
        overflow: hidden;
        height: 89px;
    }

    .formPlace{
        background-color: white;
        width: 585px;
        height: 471px;
        border-radius: 20px;
        border: 2px solid rgba(98, 72, 255, 1);
        margin: 134px 0 0 0;
        padding: 80px;
        text-align: center;
    }

    .phone > div:first-child, .email > div:first-child, .address > div:first-child {
        font-size: 1.5rem;
        line-height: 16px;
        font-weight: 500;

    }

    .phone > div:nth-child(2), .email > div:nth-child(2), .address > div:nth-child(2) {
        font-size: 1.6rem;
        line-height: 27px;
        margin-top: 8px;
    }

    .email, .address {
        margin-top: 16px;
    }

    .contactInfo {
        margin-top: 24px;
    }

    .contactInfoCont {
        margin-top: 48px;
        height: 263px;
        font-size: 1.6rem;
    }

    .content{
        height: 739px;
        display: flex;
    }

    .infoPlace{
        margin: 120px 132px 120px 120px;
        width: 483px;
        height: 499px;
    }

    .supportStaffText{
        font-size: 1.8rem;
        line-height: 30px;
        margin-top: 30px
    }

    .contactInfo a {
    text-decoration: none;
    color: rgba(79, 79, 79, 1);
    }

    .contactInfo a:hover {
        color: none;
    }

    @media only screen and (max-width: 1150px) {
        .content {
            flex-direction: column;
            padding: 48px 130px;
            height: auto;
        }

        .infoPlace {
            margin: 0;
            width: auto;
        }

        .customH2 {
            text-align: center;
        }

        .supportStaffText, .contactInfoCont {
            margin-top: 32px;
        }

        .formPlace {
            width: auto;
            height: auto;
            margin: 48px 0 0 0;
            padding: 80px 41px 80px 42px;
        }

        .customInput {
            width: 100%;
        }
    }

    @media only screen and (max-width: 670px) {
        .content {
            padding: 48px 20px;
        }

        .contactInfoCont, .infoPlace {
            height: auto;
        }

        .supportStaffText, .contactInfoCont {
            margin-top: 24px;
        }

        .customH2 {
            text-align: start;
        }

        .formPlace {
            padding: 48px 16px;
        }

    }
</style>