<template>
  <div
    :class="
      Platform.is.mobile
        ? 'column justify-center bg-dark text-grey-2'
        : 'window-height column justify-center text-grey-2 bg-dark'
    "
  >
    <span
      :class="
        Platform.is.mobile
          ? 'q-my-lg text-weight-bolder text-accent text-h2'
          : 'self-center text-h1 text-weight-bolder text-accent q-my-xl'
      "
      >Contact</span
    >

    <div
      :class="
        Platform.is.mobile
          ? 'column q-gutter-y-md q-pa-md'
          : 'row q-px-xl q-gutter-x-lg'
      "
    >
      <div
        :class="
          Platform.is.mobile
            ? 'column q-gutter-y-md'
            : 'col column q-gutter-y-lg'
        "
      >
        <span class="text-h6 text-weight-light"
          >I am open to collaborating with any company that believes my skills
          would be valuable to them. If you are seeking someone with my
          qualifications, please feel free to reach out. Alternatively, you can
          simply send a friendly greeting my way.
        </span>
        <div
          :class="
            Platform.is.mobile ? 'column q-gutter-y-md' : 'row q-gutter-x-lg'
          "
        >
          <q-btn
            outline
            color="accent"
            label="Contact Me"
            no-caps
            size="xl"
            href="mailto:ynciertocarlo84@gmail.com"
          />
          <q-btn
            outline
            color="accent"
            label="Projects"
            no-caps
            size="xl"
            @click="scrollToComponent"
          />
        </div>
      </div>
      <div class="col column q-gutter-y-md">
        <div class="column q-gutter-y-sm">
          <span class="text-h5 text-weight-bold">Email</span>
          <span class="text-h6 text-weight-light"
            >ynciertocarlo84@gmail.com</span
          >
        </div>
        <div class="column q-gutter-y-sm">
          <span class="text-h5 text-weight-bold">Address</span>
          <span class="text-h6 text-weight-light"
            >Calan 2 Poblacion, Cebu City</span
          >
        </div>
        <div class="column q-gutter-y-sm">
          <span class="text-h5 text-weight-bold">Contact Number</span>
          <span class="text-h6 text-weight-light">+639663494882 </span>
        </div>
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
