<template>
  <div style="background-color: #fff; width: 100vw">
    <v-container style="width: 90%">
      <v-row no-gutters>
        <v-col cols="justify-center">
          <div class="flex-wrap mt-15">
            <p
              style="
                font-size: 34px;
                font-weight: 500;
                color: #262626;
                line-height: 48px;
              "
            >
              Ecosystem
            </p>
            <div class="mt-14">
              <div class="image-container d-flex ga-6">
                <!-- <VueSlickCarousel :settings="settings"> -->
                <img
                  v-for="(imageUrl, index) in ecosystem_imageUrls"
                  :key="index"
                  :src="imageUrl"
                  :alt="`Chain Icon ${index}`"
                  class="img-animation-right"
                />
                <!-- </VueSlickCarousel> -->
              </div>

              <div class="image-container d-flex ga-6 mt-8">
                <img
                  v-for="(imageUrl, index) in ecosystem_imageUrls"
                  :key="index"
                  :src="imageUrl"
                  :alt="`Chain Icon ${index}`"
                  class="img-animation-left"
                />
              </div>
            </div>
          </div>
          <div
            style="
              margin-top: 90px;
              justify-content: center;
              text-align: center;
              flex-direction: column;
              width: 80vw;
            "
          >
            <div>
              <p
                style="
                  font-size: 34px;
                  font-weight: 500;
                  color: #262626;
                  line-height: 48px;
                "
              >
                The Overview of Lambda Storage Network
              </p>
              <p
                style="
                  font-size: 20px;
                  font-weight: 400;
                  color: #262626;
                  line-height: 28px;
                  margin-top: 25px;
                "
              >
                Empowering the Next Generation of Value Internet
              </p>
            </div>
            <v-container
              class="d-flex align-center xsdirection"
              style="width: 100%"
            >
              <v-col
                md="8"
                xs="12"
                class="d-flex justify-space-between mapimage1"
              >
                <div>
                  <p class="numberfont">73</p>
                  <p class="labelfont">Validators</p>
                </div>
                <div>
                  <p class="numberfont">971</p>
                  <p class="labelfont">Miners</p>
                </div>
                <div>
                  <p class="numberfont">1100</p>
                  <p class="labelfont">Mainnet Accounts</p>
                </div>
              </v-col>
              <v-col
                md="4"
                xs="12"
                class="d-flex justify-space-evenly mapimage2"
                style="width: 95vw"
              >
                <img
                  src="https://www.lambda.im/img/section3-img@1x.3bbe9f2a.png"
                  width="132"
                  height="113"
                />
                <div class="flex-column mt-13">
                  <div class="d-flex">
                    <p
                      style="
                        font-size: 80px;
                        font-weight: 700;
                        color: #3f4ae1;
                        line-height: 23px;
                        font-family: DINAlternate-Bold, DINAlternate;
                      "
                    >
                      640
                    </p>
                    <p
                      style="
                        font-size: 30px;
                        font-weight: 600;
                        color: #3f4ae1;
                        line-height: 42px;
                      "
                    >
                      PB
                    </p>
                  </div>
                  <p class="labelfont">Network Capacity 640PB</p>
                </div>
              </v-col>
            </v-container>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { ecosystem_imageUrls } from "../constants/image";

const settings = ref({
  arrows: false,
  dots: false,
  infinite: true,
  slidesToShow: 1,
  slidesToScroll: 1,
  autoplay: true,
  speed: 2000,
  autoplaySpeed: 2000,
  cssEase: "linear",
});
</script>
<style scoped>
@media (max-width: 575.98px) {
  .xsdirection {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100vw;
  }
}
.image-container {
  overflow: hidden;
  white-space: nowrap;
}

.img-animation-right {
  display: inline-block; /* Display images inline */
  animation: slideRight 2s ease-in infinite; /* Apply the slideRight animation */
  margin-right: -10px; /* Adjust margin to avoid space between images */
}

@keyframes slideRight {
  0% {
    transform: translateX(100%); /* Start position */
  }
  100% {
    transform: translateX(-100%); /* End position */
  }
}
.img-animation-left {
  display: inline-block; /* Display images inline */
  animation: slideLeft 2s ease-in infinite; /* Apply the slideRight animation */
  margin-left: -10px; /* Adjust margin to avoid space between images */
}

@keyframes slideLeft {
  0% {
    transform: translateX(-100%); /* Start position */
  }
  100% {
    transform: translateX(100%); /* End position */
  }
}

.mapimage1 {
  background: url(https://www.lambda.im/img/pc-map.ef99059d.png);
  /* width: 60%; */
  height: 455px;
  background-size: 100% 100%;
  background-repeat: no-repeat;
  position: relative;
  padding-top: 80px;
}
.numberfont {
  font-size: 50px;
  font-family: DINAlternate-Bold, DINAlternate !important;
  font-weight: 700;
  color: #3f4ae1;
  line-height: 58px;
}
.labelfont {
  font-size: 18px;
  font-weight: 600;
  color: #262626;
  line-height: 25px;
}
.mapimage2 {
  background-image: url(https://www.lambda.im/img/Rectangle\ 2@2x.c79d1ea6.png);
  margin-bottom: 50px;
  /* width: 40%; */
  height: 400px;
  background-size: 100% 100%;
  background-repeat: no-repeat;
  padding-top: 35px;
}
@media (max-width: 576px) {
  .mapimage2 {
    width: 92%;
  }
  .mapimage1 {
    width: 92%;
  }
}
</style>
