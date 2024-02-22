<template>
  <footer class="footer">
    <div class="innerCont">
      <div>
        <div class="logo">
          LOGO
        </div>
        <div class="infoAndRisk">
          <div class="gray1">
            Information and high risk warning:
          </div>
          <div class="gray2 fontMontserrat">
            Trading with foreign exchange (FX), contract for differences (CFDs) and precious metals carries a high level of risk that may not be suitable for all investors. Leverage creates additional risk and loss exposure. Before you decide to trade foreign exchange or contract for differences, carefully consider your investment objectives, experience level, and risk tolerance.
          </div>
        </div>
        <div class="legalDisclaimer">
          <div class="gray1">
            Legal disclaimer:
          </div>
          <div class="gray2 fontMontserrat">
            Forex trading entails significant risks and is not appropriate for all investors. The possibility of incurring substantial losses should be taken into account. It is therefore important to understand the possible consequences of investing. Traders should weigh their earning potential against the risks involved and act accordingly. Interactive Trade Ltd operating under brand and using domenLink domain within the European Economic Area.
          </div>
        </div>
        <div class="aboutUs gray1 fontWeigth500">
          <div>About us</div>
          <div>Instructions</div>
          <div>Platforms</div>
          <div>Contact Us</div>
          <div>Sign in</div>
          <div>Sign up for free</div>
        </div>
      </div>
      <div class="gray3 fontWeigth400 fontMontserrat copyrights">
        <div>Copyright 2020, All Right Reserved</div>
        <div>Terms and Conditions</div>
        <div>Privacy Policy</div>
        <div>Risk Warnings</div>
        <div>Anti-Money Laundering</div>
      </div>
    </div>
  </footer>
</template>

<script>
export default{
    name: 'AppFooter',

}
</script>

<style scoped>
    .footer {
        padding: 32px 120px;
    }

    .innerCont > div:first-child {
        display: flex;
    }
    .infoAndRisk {
        margin-left: 160px;
        width: 380px;
    }

    .legalDisclaimer {
        margin-left: 30px;
        width: 380px;
    }

    .infoAndRisk > div:first-child, .legalDisclaimer > div:first-child {
        font-size: 1.8rem;
        font-weight: 500;
        line-height: 30px;
    }

    .infoAndRisk > div:last-child, .legalDisclaimer > div:last-child {
        margin-top: 16px;
        font-size: 1.6rem;
        font-weight: 400;
        line-height: 27px;
    }

    .aboutUs {
        margin-left: 96px;
        display: flex;
        flex-direction: column;
        gap: 24px;
        font-size: 1.5rem;
        line-height: 16px;
    }

    .logo{
        color: rgba(0, 0, 0, 1);
        font-size: 1.5rem;
        font-weight: 700;
    }

    .copyrights > div:nth-child(2), .copyrights > div:nth-child(3), .copyrights > div:nth-child(4) {
        margin-right: 66px;
    }

    .copyrights > div:first-child {
        margin-right: 132px;
    }

    .copyrights{
        font-size: 1.6rem;
        line-height: 27px;
        display: flex;
        margin-top: 48px;
    }

    @media only screen and (max-width: 1150px) {
        .footer {
            padding: 0 40px 48px;
        }

        .innerCont > div:first-child {
            flex-direction: column;
        }

        .logo {
            order: 1;
            text-align: center;
            margin-top: 62px;
        }

        .aboutUs {
            order: 2;
            flex-direction: row;
            margin: 0;
            margin-top: 54px;
            justify-content: space-between;
        }

        .infoAndRisk {
            order: 3;
            margin: 0;
            width: 508px;
            height: 208px;
            margin: 40px auto 0;
        }

        .legalDisclaimer {
            order: 4;
            margin: 0;
            width: 508px;
            height: 262px;
            margin: 32px auto 0;
        }

        .legalDisclaimer > div:first-child, .infoAndRisk > div:first-child {
            text-align: center;
        }

        .copyrights {
            flex-direction: column;
            margin-top: 40px;
            align-items: center;
            gap: 16px;
        }

        .copyrights > div:first-child,
        .copyrights > div:nth-child(2),
        .copyrights > div:nth-child(3),
        .copyrights > div:nth-child(4)  {
            margin: 0;
        }
    }

    @media only screen and (max-width: 670px) {
        .footer {
            padding: 0 20px 32px;
        }

        .aboutUs {
            flex-direction: column;
        }

        .infoAndRisk, .legalDisclaimer  {
            width: auto;
            height: auto;
        }

        .legalDisclaimer > div:first-child, .infoAndRisk > div:first-child {
            text-align: left;
        }
        .legalDisclaimer {
            margin-top: 24px;
        }

        .copyrights, .logo, .aboutUs {
            margin-top: 32px;
        }
    }
</style>