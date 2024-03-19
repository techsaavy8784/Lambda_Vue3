<template>
  <v-app style="position: fixed; z-index: 10">
    <v-app-bar
      class="justify-center flex-wrap"
      style="box-shadow: none; position: fixed; background: transparent"
    >
      <v-btn
        v-for="(item, index) in items"
        :key="index"
        :style="getButtonStyle(index)"
      >
        {{ item }}
      </v-btn>
    </v-app-bar>
  </v-app>
</template>

<script setup lang="ts">
import { onMounted, onBeforeUnmount, ref } from "vue";
const items = ref(["Storage", "Explorer", "GetLAMB"]);
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
}
</style>
