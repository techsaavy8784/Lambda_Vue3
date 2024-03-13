<template>
  <div class="newsbackground">
    <v-container style="width: 80%; padding: 1px !important">
      <v-row class="justify-center align-center mt-10 mb-10">
        <p
          style="
            font-size: 34px;
            font-weight: 600;
            color: #262626;
            line-height: 48px;
          "
        >
          Latest News
        </p>
      </v-row>
      <v-row
        class="justify-center align-center ga-10 xsdirection d-flex"
        style="padding-bottom: 100px"
      >
        <div
          class="flex-column flex"
          v-for="(newsItem, index) in newsData"
          :key="index"
          style="box-shadow: 1px 3px 22px 0 #e6e4fe; border: 1px solid #e8e8e8"
        >
          <div>
            <img
              :src="newsItem.img"
              alt="picture"
              class="xswidth"
              width="250px"
            />
          </div>
          <div
            style="
              width: 250px;
              padding: 15px;
              text-align: center;
              background-color: #fff;
              color: #262626;
            "
          >
            <p>{{ newsItem.title }}</p>
          </div>
        </div>
      </v-row>
    </v-container>
  </div>
</template>

<script setup lang="ts">
import { newsData } from "../constants/newsdata";
</script>

<style>
.newsbackground {
  width: 100vw;
  background-color: #fff;
}
@media (max-width: 575.98px) {
  .xsdirection {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .xswidth {
    width: 100%;
  }
}
</style>
