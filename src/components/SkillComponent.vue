<template>
  <div
    :class="
      Platform.is.mobile
        ? 'window-height column justify-center bg-dark text-grey-2 q-gutter-y-md q-pa-md'
        : 'window-height column justify-center bg-dark text-grey-2 q-gutter-y-xl'
    "
  >
    <span
      :class="
        Platform.is.mobile
          ? 'text-h3 text-weight-bolder text-grey-2'
          : 'q-ml-xl text-h3 text-weight-bolder text-grey-2'
      "
      >My Skills</span
    >

    <div
      :class="
        Platform.is.mobile
          ? 'column q-gutter-y-md justify-center'
          : 'row justify-center q-gutter-lg q-pa-lg'
      "
    >
      <div
        :class="
          Platform.is.mobile
            ? 'column q-gutter-y-sm'
            : 'col-5 column q-gutter-y-sm'
        "
      >
        <div class="row justify-between">
          <span class="text-h5 text-accent text-weight-bold">JavaScript</span>
          <span class="text-h5 text-accent text-weight-bold">78%</span>
        </div>
        <q-linear-progress
          rounded
          size="15px"
          :value="0.78"
          track-color="grey-1"
          color="accent"
          class="q-mt-sm"
        />
      </div>

      <div
        :class="
          Platform.is.mobile
            ? 'column q-gutter-y-sm'
            : 'col-5 column q-gutter-y-sm'
        "
      >
        <div class="row justify-between">
          <span class="text-h5 text-accent text-weight-bold">HTML-5</span>
          <span class="text-h5 text-accent text-weight-bold">88%</span>
        </div>
        <q-linear-progress
          rounded
          size="15px"
          :value="0.88"
          track-color="grey-1"
          color="accent"
          class="q-mt-sm"
        />
      </div>

      <div
        :class="
          Platform.is.mobile
            ? 'column q-gutter-y-sm'
            : 'col-5 column q-gutter-y-sm'
        "
      >
        <div class="row justify-between">
          <span class="text-h5 text-accent text-weight-bold">CSS3</span>
          <span class="text-h5 text-accent text-weight-bold">67%</span>
        </div>
        <q-linear-progress
          rounded
          size="15px"
          :value="0.67"
          track-color="grey-1"
          color="accent"
          class="q-mt-sm"
        />
      </div>

      <div
        :class="
          Platform.is.mobile
            ? 'column q-gutter-y-sm'
            : 'col-5 column q-gutter-y-sm'
        "
      >
        <div class="row justify-between">
          <span class="text-h5 text-accent text-weight-bold">VUEjs</span>
          <span class="text-h5 text-accent text-weight-bold">70%</span>
        </div>
        <q-linear-progress
          rounded
          size="15px"
          :value="0.7"
          track-color="grey-1"
          color="accent"
          class="q-mt-sm"
        />
      </div>
    </div>

    <q-btn
      outline
      color="accent"
      label="Contact"
      no-caps
      :class="Platform.is.mobile ? 'self-start' : 'q-ml-xl self-start'"
      size="xl"
      @click="scrollToComponent"
    />
  </div>
</template>

<script setup>
import { Platform } from "quasar";

const emits = defineEmits(["wantAScroll"]);

const scrollToComponent = () => {
  emits("wantAScroll");
};
</script>
