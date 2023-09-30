<template>
  <q-page>
    <div class="col-12" :class="viewScreen ? 'q-pa-none' : 'q-pa-xl'">
      <div
        v-show="!viewScreen"
        style="
          color: red;
          font-size: 120px;
          height: fit-content;
          margin: 0px 0px -60px 30px;
        "
      >
        News
      </div>
      <div
        class="row"
        style="background-color: red; height: 320px; border-radius: 20px"
      >
        <div :class="viewScreen ? 'newsMobile' : 'newsDesktop'">
          <div
            v-show="$q.screen.lt.md"
            style="font-size: 16px; height: fit-content"
          >
            News
          </div>
          <div :class="viewScreen ? 'newsTitleMobile' : 'newsTitleDesktop'">
            Lorem Ipsum
          </div>
          <div :class="viewScreen ? 'newsContentMobile' : 'newsContentDesktop'">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit.<br />
            Suspendisse ullamcorper egestas augue, in fringilla ipsum<br />
            condimentum at.
          </div>
        </div>
        <div class="col-6">
          <q-img
            class="q-pb-xl absolute"
            src="src/assets/frame1.svg"
            style="
              border-radius: 20px;
              height: 500px;
              width: 420px;
              left: 700px;
              bottom: 10px;
            "
          />
          <div
            class="absolute q-px-lg"
            flat
            style="
              background-color: #ffffff;
              box-shadow: 0 0, -1px 0 10px rgb(0, 0, 0, 0.1);
              border-radius: 30px;
              bottom: 75px;
            "
          >
            <div style="margin-bottom: -30px">
              <div
                style="font-size: 20px"
                class="full-width flex justify-center"
              >
                Learn from best
              </div>
              <div
                style="font-size: 20px"
                class="full-width flex justify-center"
              >
                <span style="color: #96c67f">instructors</span>&nbsp; around
              </div>
              <div
                style="font-size: 20px"
                class="full-width flex justify-center"
              >
                the globe
              </div>
            </div>
            <div class="flex justify-center">
              <q-img
                src="src/assets/frame2.svg"
                style="height: 50px; width: 50px"
              />
              <q-img
                src="src/assets/frame2.svg"
                style="height: 50px; width: 50px; margin-left: -20px"
              />
              <q-img
                src="src/assets/frame2.svg"
                style="height: 50px; width: 50px; margin-left: -20px"
              />
              <q-img
                src="src/assets/frame2.svg"
                style="height: 50px; width: 50px; margin-left: -20px"
              />
              <q-img
                src="src/assets/frame2.svg"
                style="height: 50px; width: 50px; margin-left: -20px"
              />
            </div>
          </div>
          <div
            class="absolute flex flex-center column q-pa-md"
            flat
            style="
              background-color: #ffffff;
              border-radius: 30px;
              bottom: 30px;
              right: 80px;
            "
          >
            <div
              style="
                background-color: #e4f9db;
                border-radius: 30px;
                width: fit-content;
              "
              class="flex justify-center q-pa-sm"
            >
              <q-icon name="person" color="positive" />
            </div>
            <div
              class="flex justify-center"
              style="font-size: 24px; color: #96c67f"
            >
              15K
            </div>
            <div class="flex justify-center" style="font-size: 12px">
              Amazing students<br />
              around the globe
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
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
.newsMobile {
  display: flex;
  flex-direction: column;
  justify-content: left;
  align-self: center;
  font-weight: bold;
}
.newsDesktop {
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-weight: bold;
}
.newsTitleDesktop {
  font-size: 60px;
  height: fit-content;
  font-weight: bold;
  padding-left: 30px;
}

.newsTitleMobile {
  font-size: 20px;
  height: fit-content;
  font-weight: bold;
  padding-left: 30px;
}
.newsContentDesktop {
  height: fit-content;
  font-size: 16px;
  padding-left: 30px;
}
.newsContentMobile {
  height: fit-content;
  font-size: 14px;
  padding-left: 30px;
}
</style>
