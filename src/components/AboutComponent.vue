<style lang="sass" scoped>
.picture
  -webkit-filter: brightness(110%) contrast(110%) grayscale(100%)
  filter: brightness(110%) contrast(110%) grayscale(100%)
  transition: 500ms cubic-bezier(0.12, 0, 0.39, 0)

  &:hover
    -webkit-filter: contrast(90%) sepia(20%)
    filter: contrast(90%) sepia(20%)
</style>

<template>
  <div
    :class="
      Platform.is.mobile
        ? 'window-height column justify-center bg-dark text-grey-2'
        : 'window-height column justify-center bg-dark text-grey-2'
    "
  >
    <div
      :class="
        Platform.is.mobile
          ? 'column reverse items-center q-pa-md'
          : 'row q-px-xl q-gutter-x-lg items-center'
      "
    >
      <div class="col column q-gutter-y-md">
        <span
          :class="
            Platform.is.mobile
              ? 'text-center text-subtitle1 text-weight-light'
              : 'text-h6 text-weight-light'
          "
        >
          Hello everyone!! I'm Carlo Yncierto, a committed software engineer
          with a focus on developing web, mobile, and desktop applications. My
          proficiency lies in JavaScript, and my goal is to enhance web
          accessibility. I currently achieving my Bachelor's Degree in
          Information Technology at Cordova Public College. I am enthusiastic
          about exploring career opportunities that align with my passion and
          skills.
        </span>
        <q-btn
          outline
          color="accent"
          label="Skills"
          no-caps
          class="self-start"
          size="xl"
          @click="scrollToComponent"
        />
      </div>
      <div :class="Platform.is.mobile ? 'column ' : 'col column items-center'">
        <img
          class="picture rounded-borders"
          src="~assets/picture.png"
          style="width: 300px"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { Platform } from "quasar";

const emits = defineEmits(["wantAScroll"]);

const scrollToComponent = () => {
  emits("wantAScroll");
};
</script>
