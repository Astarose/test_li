<template>
  <div
    class="col-12 q-pa-lg"
    style="height: 390px; background-color: black; color: white"
  >
    <div>
      <div class="row">
        <div class="col-4 flex">
          <div style="font-size: 32.8px">Lorem ipsum</div>
          <div style="font-size: 16px" v-show="!viewScreen">
            <div>
              we are not here to sell you products,<br />we sell value through
              our experience
            </div>
          </div>
          <div class="row flex align-end q-mt-xl">
            <q-img
              class="q-ma-sm"
              src="src/assets/logoFacebook.svg"
              style="height: 24px; width: 24px"
            ></q-img>
            <q-img
              class="q-ma-sm"
              src="src/assets/logoTwitter.svg"
              style="height: 24px; width: 24px"
            ></q-img>
            <q-img
              class="q-ma-sm"
              src="src/assets/logoInstagram.svg"
              style="height: 24px; width: 24px"
            ></q-img>
            <q-img
              class="q-ma-sm"
              src="src/assets/logoLinkedin.svg"
              style="height: 24px; width: 24px"
            ></q-img>
          </div>
        </div>
        <div class="col-8">
          <div class="flex">
            <q-list style="width: fit-content">
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
                <q-item-section> Resources </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Contact us </q-item-section>
              </q-item>
            </q-list>
            <q-list style="width: fit-content">
              <q-item clickable>
                <q-item-section> SME </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Solution </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Reviews </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Blog </q-item-section>
              </q-item>
            </q-list>
            <q-list style="width: fit-content">
              <q-item clickable>
                <q-item-section> Contact Us </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Place A Call </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Email </q-item-section>
              </q-item>
            </q-list>
            <q-list style="width: fit-content" v-show="!viewScreen">
              <q-item clickable>
                <q-item-section> Job Opening </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> News </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Research </q-item-section>
              </q-item>
            </q-list>
            <q-list style="width: fit-content" v-show="!viewScreen">
              <q-item clickable>
                <q-item-section> UK Privacy Policy </q-item-section>
              </q-item>
              <q-item clickable>
                <q-item-section> Terms Of Use </q-item-section>
              </q-item>
            </q-list>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-12 flex flex-center q-gutter-y-md">
          <div class="full-width flex justify-center">
            Subscribe to get latest updates
          </div>
          <div class="flex justify-center full-width">
            <q-input
              filled
              outlined
              :style="{ width: viewScreen ? '80%' : '30%' }"
              dense
              placeholder="Your Email address"
              class="custom-input"
            />

            <q-btn
              square
              no-caps
              flat
              label="Submit"
              style="background-color: #96c67f"
            />
          </div>
        </div>
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
<style>
.custom-input {
  background-color: white;
}
</style>
