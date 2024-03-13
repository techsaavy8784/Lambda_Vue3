<template>
  <div style="background-color: #fff; width: 100vw">
    <v-container style="width: 90%">
      <v-row no-gutters>
        <v-col cols="justify-center d-flex flex-column">
          <div class="logo_container">
            <p
              style="
                text-align: center;
                color: #262626;
                font-size: 34px;
                font-weight: 600;
                margin-top: 20px;
              "
            >
              Build on any blockchain with Lambda
            </p>
            <div class="d-flex justify-space-between mt-9 px-14 align-center">
              <img
                v-for="(imageUrl, index) in first_imageUrls"
                :key="index"
                :src="imageUrl"
                :alt="`Chain Icon ${index}`"
                style="width: 50px; height: 50px"
              />
            </div>
            <div
              class="d-flex justify-space-between mt-9 mb-14 px-14 align-center"
            >
              <img
                v-for="(imageUrl, index) in second_imageUrls"
                :key="index"
                :src="imageUrl"
                :alt="`Chain Icon ${index}`"
                :style="getImageStyle(index)"
              />
            </div>
          </div>
          <div
            class="d-flex align-center justify-center ga-15 mt-15 flex-wrap secondPart_font_family"
            style="color: #3f4ae1"
          >
            <div>
              <p style="font-size: 20px; font-weight: 500 !important">
                TYPICAL APY
              </p>
              <p
                style="
                  font-size: 90px;
                  font-weight: 700 !important;
                  line-height: 80px;
                "
              >
                42.04%
              </p>
            </div>
            <div>
              <p style="font-weight: bold; font-size: 24px; color: #262626">
                Staking LAMB to earn rewards
              </p>
              <p style="line-height: 24px; font-size: 20px; color: #333">
                When staking is complete, rewards will start to calculated<br />
                immediately. At any time, stakers can claim their cumulative<br />
                reward through dApp.
              </p>
            </div>
          </div>
          <div
            class="xsdirection d-flex justify-space-evenly secondPart_font_family align-center flex-wrap"
            style="margin-top: 50px"
          >
            <div>
              <p style="line-height: 24px; color: #333">IF YOU STAKE</p>
              <p
                style="
                  font-size: 60px;
                  font-weight: bold;
                  color: #474747;
                  line-height: 70px;
                "
              >
                2,000
              </p>
              <p style="line-height: 24px; color: #333">LAMB</p>
            </div>
            <div class="bg-rewards">
              <p class="rewards-text bold">YOUR REWARDS</p>
              <p class="rewards-number mt-5">798.74</p>
            </div>
            <div>
              <p
                style="
                  font-size: 60px;
                  font-weight: bold;
                  color: #474747;
                  line-height: 70px;
                "
              >
                5%
              </p>
              <p style="line-height: 24px; color: #333">COMMISSION</p>

              <p style="line-height: 24px; color: #333">
                (Varies between validators)
              </p>
            </div>
          </div>
          <button
            class="mt-15 secondPart_font_family bold"
            style="
              background-color: #3f4ae1;
              cursor: pointer;
              font-weight: 700;
              font-size: 30px;
              border-radius: 16px;
              padding-top: 20px;
              padding-bottom: 20px;
            "
          >
            Staking LAMB
          </button>
          <p
            style="
              font-size: 34px;
              color: #262626;
              line-height: 48px;
              margin-top: 80px;
              text-align: center;
            "
          >
            DAPP based on LambdaNetwork
          </p>
          <div
            class="d-flex align-center justify-space-evenly flex-wrap"
            style="margin-top: 100px"
          >
            <div class="flex-column">
              <div class="d-flex align-center ga-4">
                <img
                  src="https://www.lambda.im/img/section8-logo1.7b4d1035.png"
                  width="72"
                />
                <p
                  class="secondPart_font_family"
                  style="font-weight: 600; font-size: 60px; color: #1e1e1e"
                >
                  Genify
                </p>
              </div>
              <p
                style="margin-top: 20px; color: #434343"
                class="secondPart_font_family"
              >
                The first innovative, open, creator-friendly, generative art<br />
                platform where users from any blockchain ecosystem can create<br />
                and collect generative art.
              </p>
              <button
                class="secondPart_font_family"
                style="
                  background-color: #3f4ae1;
                  cursor: pointer;
                  font-weight: 400;
                  font-size: 25px;
                  border-radius: 10px;
                  width: 170px;
                  height: 64px;
                  margin-top: 40px;
                "
              >
                Get LAMB
              </button>
            </div>
            <img
              src="https://www.lambda.im/img/section8-img.21546110.png"
              class="xswidth"
            />
          </div>
          <div
            class="d-flex align-center justify-space-evenly flex-wrap"
            style="margin-top: 70px"
          >
            <img
              src="https://www.lambda.im/img/section8-img2.0f4db228.png"
              class="xswidth"
            />
            <div class="flex-column">
              <div class="d-flex align-center ga-4">
                <img
                  src="data:image/png;base64,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"
                  width="72"
                />
                <p
                  class="secondPart_font_family"
                  style="font-weight: 600; font-size: 60px; color: #1e1e1e"
                >
                  Tagge
                </p>
              </div>
              <p
                style="margin-top: 20px; color: #434343"
                class="secondPart_font_family"
              >
                Be the first to discover some epic Web3 content.Never miss
                out<br />
                on any opportunities, events, knowledges, and news.
              </p>
              <button
                class="secondPart_font_family"
                style="
                  background-color: #3f4ae1;
                  cursor: pointer;
                  font-weight: 400;
                  font-size: 25px;
                  border-radius: 10px;
                  width: 170px;
                  height: 64px;
                  margin-top: 40px;
                "
              >
                Get LAMB
              </button>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup lang="ts">
import { first_imageUrls } from "../constants/image";
import { second_imageUrls } from "../constants/image";

const getImageStyle = (index: number) => {
  if (index === 2) {
    return {
      width: "150px",
      height: "20px",
    };
  }
  return {
    width: "50px",
    height: "50px",
  };
};
</script>
<style>
@media (max-width: 575.98px) {
  .xsdirection {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .xswidth {
    width: 100%;
  }
  .logo_container .d-flex {
    flex-wrap: wrap;
  }
  .logo_container img {
    width: 25%;
    height: auto;
  }
  .bg-rewards {
    width: 100% !important;
  }
}

.rewards-text {
  font-size: 16px;
  color: "#fff";
}
.rewards-number {
  font-weight: 700;
  font-size: 48px;
  color: "#fff";
}
.bg-rewards {
  justify-content: center; /* Centers children horizontally - optional for vertical centering */
  align-items: center; /* Centers children vertically */
  flex-direction: column;
  text-align: center;
  width: 40%;
  height: 340px;
  background: url(https://www.lambda.im/img/rewards.fe9df074.png) 50% no-repeat;
}
.bg-rewards > * {
  position: relative;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
}
.logo_container {
  width: 100%;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 10px 10px 0 rgba(111, 153, 223, 0.07),
    0 0 33px 0 rgba(151, 154, 194, 0.29);
  margin-top: -80px;
}
.secondPart_font_family {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>
