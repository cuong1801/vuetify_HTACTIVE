<template>
  <v-container class="grey lighten-5">
    <v-row no-gutters>
      <v-col cols="12" sm="6" md="8">
        <app-content></app-content>
      </v-col>
      <v-col cols="6" md="4">
        <app-menu-left></app-menu-left>
      </v-col>
    </v-row>
    <v-divider></v-divider>
    <app-review></app-review>
    <v-divider></v-divider>
    <app-list-task style="padding:12px"></app-list-task>
    <v-divider></v-divider>
    <app-body></app-body>
    <v-divider></v-divider>
    <app-footer></app-footer>
    <v-divider></v-divider>
  </v-container>
</template>

<script>
import AppMenuLeft from "./MenuLeft.vue";
import AppContent from "./Content.vue";
import AppFooter from "./Footer.vue";
import AppReview from "./Review.vue";
import AppBody from "./Body.vue";
import AppListTask from "./ListTask.vue";

export default {
  name: "HelloWorld",
  components: {
    AppMenuLeft,
    AppContent,
    AppFooter,
    AppReview,
    AppBody,
    AppListTask
  },
  data: () => ({
    return: {
      home: "home",
      right: null
    },

    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader"
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify"
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify"
      }
    ],
    importantLinks: [
      {
        text: "Documentation",
        href: "https://vuetifyjs.com"
      },
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com"
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify"
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs"
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify"
      }
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com/components/api-explorer"
      },
      {
        text: "Select a layout",
        href: "https://vuetifyjs.com/layout/pre-defined"
      },
      {
        text: "Frequently Asked Questions",
        href: "https://vuetifyjs.com/getting-started/frequently-asked-questions"
      }
    ]
  })
};
</script>
