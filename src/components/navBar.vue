<template>
  <link
    href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap"
    rel="stylesheet"
  />
  <div class="row">
    <div
      class="col-4 flex justify-center"
      style="color: black; font-size: 32.8px"
    >
      <q-btn v-show="!viewScreen" icon="menu" flat>
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
    <div class="col-5" v-show="viewScreen">
      <q-list class="flex" v-show="viewScreen">
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
    <div class="col-3 flex flex-center">
      <div v-show="viewScreen">
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
  if ($q.screen.lt.md == true) {
    return false;
  } else {
    return true;
  }
});
</script>
