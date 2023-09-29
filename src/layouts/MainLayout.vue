<template>
  <q-layout>
    <nav-bar></nav-bar>
    <q-page-container>
      <router-view />
    </q-page-container>
    <q-footer></q-footer>
  </q-layout>
</template>

<script setup>
import navBar from "src/components/navBar.vue";
import qFooter from "src/components/qFooter.vue";
</script>
