<template>
  <v-app id="inspire">
    <v-app-bar
      class="justify-center"
      style="
        background-color: #4953e8;
        box-shadow: none;
        height: 64px !important;
        /* background: transparent; */
      "
    >
      <v-btn style="background: transparent; margin: 0 auto">Storage</v-btn>
      <v-btn style="background: transparent; margin: 0 auto">Explorer</v-btn>
      <v-btn style="background: transparent; margin: 0 auto">Docs</v-btn>
      <v-btn style="background: transparent; margin: 0 auto">English</v-btn>
      <v-btn
        style="
          border-radius: 6px;
          padding: 5px 20px;
          background: #9155fd;
          margin: 0 auto;
        "
        >English</v-btn
      >
    </v-app-bar>
  </v-app>
</template>

<script setup lang="ts"></script>

<style>
.v-application__wrap {
  min-height: 64px;
}
</style>
