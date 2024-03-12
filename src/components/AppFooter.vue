<template>
  <v-footer app style="padding-top: 50px; background-color: #2d3969">
    <v-col md="3" xs="6" class="vcol">
      <a
        v-for="item in items"
        :key="item.title"
        :href="item.href"
        :title="item.title"
        class="d-inline-block mx-2 social-link"
        rel="noopener noreferrer"
        target="_blank"
      >
        <v-icon :icon="item.icon" :size="item.icon === '$vuetify' ? 24 : 16" />
      </a>
    </v-col>
    <v-col md="3" xs="6"><p>Home</p></v-col>
    <v-col md="2" xs="6"><p>About Lambda</p></v-col>
    <v-col md="2" xs="6"><p>Docs</p></v-col>
    <v-col md="2" xs="6"><p>Ecosystem</p></v-col>
  </v-footer>
</template>

<script setup lang="ts">
const items = [
  {
    title: "Vuetify Documentation",
    icon: `$vuetify`,
    href: "https://vuetifyjs.com/",
  },
  {
    title: "Vuetify Support",
    icon: "mdi-shield-star-outline",
    href: "https://support.vuetifyjs.com/",
  },
  {
    title: "Vuetify X",
    icon: `svg:M2.04875 3.00002L9.77052 13.3248L1.99998 21.7192H3.74882L10.5519 14.3697L16.0486 21.7192H22L13.8437 10.8137L21.0765 3.00002H19.3277L13.0624 9.76874L8.0001 3.00002H2.04875ZM4.62054 4.28821H7.35461L19.4278 20.4308H16.6937L4.62054 4.28821Z`,
    href: "https://x.com/vuetifyjs",
  },
  {
    title: "Vuetify GitHub",
    icon: `mdi-github`,
    href: "https://github.com/vuetifyjs/vuetify",
  },
  {
    title: "Vuetify Discord",
    icon: `mdi-discord`,
    href: "https://community.vuetifyjs.com/",
  },
  {
    title: "Vuetify Reddit",
    icon: `mdi-reddit`,
    href: "https://reddit.com/r/vuetifyjs",
  },
];
</script>

<style>
.vcol {
  justify-content: center;
  font-family: DINAlternate-Bold, DINAlternate !important;
  color: #fff;
  font-size: 14px;
  line-height: 23px;
  font-weight: 500;
}
</style>
