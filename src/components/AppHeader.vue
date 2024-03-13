<template>
  <v-app id="inspire" style="position: fixed">
    <!-- v-if="!drawer" -->
    <v-app-bar
      class="justify-center flex-wrap"
      style="box-shadow: none; position: fixed; background: transparent"
    >
      <!-- class="d-none d-sm-flex" -->
      <v-btn
        v-for="(item, index) in items"
        :key="index"
        :style="getButtonStyle(index)"
      >
        {{ item }}
      </v-btn>

      <!-- <v-app-bar-nav-icon
        @click="drawer = !drawer"
        class="d-flex d-sm-none"
      ></v-app-bar-nav-icon> -->
    </v-app-bar>
    <!-- 
    <v-navigation-drawer
      v-model="drawer"
      temporary
      style="background-color: #fff; width: 80vw; height: 100vh"
    >
      <v-list nav dense>
        <v-list-item
          v-for="item in items"
          :key="item"
          @click="handleItemClick(item)"
        >
          <v-list-item-title>{{ item }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
  </v-app>
</template>

<script setup lang="ts">
import { onMounted, onBeforeUnmount, ref } from "vue";

const drawer = ref(false);
const items = ref(["Storage", "Explorer", "GetLAMB"]);
const handleItemClick = (item) => {
  // Handle item click action here
  console.log(`Clicked on: ${item}`);
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleScroll);
});

function handleScroll() {
  const appBar = document.querySelector(".v-app-bar");

  if (window.scrollY > 50) {
    appBar?.classList.add("active");
  } else {
    appBar?.classList.remove("active");
  }
}

const getButtonStyle = (index: number) => {
  if (index === 2) {
    return {
      padding: "5px 20px",
      borderRadius: "6px",
      background: "#9155fd",
      color: "#fff",
      margin: "0 auto",
      textTransform: "capitalize !important",
    };
  }
  return {
    background: "transparent",
    margin: "0 auto",
    textTransform: "capitalize !important",
  };
};
</script>

<style>
.v-application__wrap {
  min-height: 64px;
}
.active {
  background-color: #4953e8 !important;
}
@media (max-width: 575.98px) {
  .xsdirection {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  /* .xswidth {
    width: 100%;
  } */
}
</style>
