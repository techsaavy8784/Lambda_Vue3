<template>
  <div class="fivebackground">
    <v-container style="width: 70%">
      <v-row class="justify-center items-center flex flex-column">
        <v-col cols="justify-center flex-column ga-10">
          <div class="flex justify-space-between">
            <p class="fivefont" style="margin-top: 45px">Lambda Milestones</p>
            <div class="d-flex"></div>
          </div>
        </v-col>
        <v-col
          cols="justify-center"
          style="margin-top: 50px; margin-bottom: 90px"
        >
          <swiper
            :navigation="true"
            :modules="modules"
            :options="swiperOptions"
            style="width: 70%"
            class="xsswiperwidth"
          >
            <swiper-slide v-for="(slide, index) in slides" :key="index">
              <div class="flex-column justify-center">
                <div class="circle">{{ slide.date }}</div>
                <p
                  style="
                    font-size: 14px;
                    color: #262626;
                    line-height: 25px;
                    text-align: center;
                  "
                >
                  {{ slide.label }}
                </p>
              </div>
            </swiper-slide>
          </swiper>
          <!-- </div> -->
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script setup lang="ts">
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import { ref } from "vue";
// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";

import "../styles/style.css";

// import required modules
import { Navigation } from "swiper/modules";
import { SwiperOptions } from "swiper/types";

interface Slide {
  date: string;
  label: string;
}

const slides = ref<Slide[]>([
  { date: "2017.12", label: "Launched Lambda project" },
  { date: "2018.6", label: "Released Whitepaper" },
  { date: "2018.8", label: "Launched Lambda project" },
  { date: "2018.9", label: "Released PoST Algorithm" },
  { date: "2018.11", label: "Released Open source core code" },
  { date: "2019.3", label: "Launched Lambda testnet" },
  { date: "2019.9", label: "Launched Lambda 4.0" },
  { date: "2020 Q1-Q2", label: "Launched Lambda 4.0" },
  { date: "2020 Q3-Q4", label: "Launched Lambda 4.0" },
  { date: "2021 Q1-Q2", label: "Launched Lambda 4.0" },
]);
const swiperOptions = {
  slidesPerView: 4,
} as SwiperOptions;
const modules = ref([Navigation]);
</script>

<style>
.fivebackground {
  width: 100vw;
  background-color: #fff;
}
.fivefont {
  font-size: 36px;
  font-weight: 600;
  color: #262626;
  line-height: 50px;
}

.items-center {
  align-items: center;
}
.circle {
  margin: 0 auto;
  width: 90px;
  height: 90px;
  background: #3f4ae1;
  border-radius: 45px;
  line-height: 90px;
  text-align: center;
  color: #fff;
  font-size: 14px;
  margin-bottom: 33px;
}
@media (max-width: 575.98px) {
  .xsswiperwidth {
    width: 100% !important;
  }
}
</style>
