<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./image/logo_red.png"
          transition="scale-transition"
          width="150"
        />
      </div>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <Demo />
    </v-content>
  </v-app>
</template>

<script>
import Demo from "./components/Demo.vue";

export default {
  name: "App",

  components: {
    Demo
  },

  data: () => ({
    //
  })
};
</script>
