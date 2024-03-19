<template>
  <v-footer app style="padding-top: 57px; background-color: #2d3969">
    <v-row style="margin: -9px !important">
      <v-col md="6" xs="12" class="vcol">
        <v-row>
          <v-col md="6" xs="6"><p style="text-align: center">Home</p></v-col>
          <v-col md="6" xs="6"
            ><p style="text-align: center">About Lambda</p></v-col
          >
        </v-row>
      </v-col>
      <v-col md="6" xs="12" class="vcol">
        <v-row>
          <v-col md="6" xs="6"><p style="text-align: center">Docs</p></v-col>
          <v-col md="6" xs="6"
            ><p style="text-align: center">Ecosystem</p></v-col
          >
        </v-row>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script setup lang="ts"></script>

<style>
.vcol {
  justify-content: center;
  color: #fff;
  font-size: 14px;
  line-height: 23px;
  font-weight: 500;
}
</style>
