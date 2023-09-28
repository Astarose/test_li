<template>
  <q-layout>
    <nav-bar></nav-bar>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import navBar from "src/components/navBar.vue";
</script>
