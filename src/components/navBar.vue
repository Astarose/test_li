<template>
  <link
    href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap"
    rel="stylesheet"
  />
  <div class="row">
    <div
      class="col-md-4 flex flex-center"
      style="color: black; font-size: 32.8px"
    >
      <q-btn v-show="viewScreen" icon="menu" flat>
        <q-menu>
          <q-list>
            <q-item clickable>
              <q-item-section> Home </q-item-section>
            </q-item>
            <q-item clickable>
              <q-item-section> Courses </q-item-section>
            </q-item>
            <q-item clickable>
              <q-item-section> Instructors </q-item-section>
            </q-item>
            <q-item clickable>
              <q-item-section> Contact </q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
      <div>Lorem Ipsum</div>
    </div>
    <q-icon
      name="account_circle"
      size="24px"
      class="flex align-center"
      v-show="viewScreen"
    />
    <div class="col-5">
      <q-list class="flex" v-show="!viewScreen">
        <q-item clickable>
          <q-item-section> Home </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section> Courses </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section> Instructors </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section> Contact </q-item-section>
        </q-item>
      </q-list>
    </div>
    <div class="col-md-3 flex flex-center">
      <div v-show="!viewScreen">
        <q-icon name="search" size="24px" class="align-center" />
        <q-btn flat dense style="color: #96c67f" label="Login" />
        <q-btn
          flat
          dense
          style="background: #96c67f; color: #ffffff"
          label="Register"
          class="q-ma-sm"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { useQuasar } from "quasar";
import { computed } from "vue";
const $q = useQuasar();
const viewScreen = computed(() => {
  return $q.screen.lt.md;
});
</script>
