<template>
  <v-card
    height="500"
    width="400"
    class="mx-auto"
  >
    <v-navigation-drawer permanent  height="500"
    width="400">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Làm 1 cái gì đó
          </v-list-item-title>
          <v-list-item-subtitle>
            Chọn cái gì đó
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <app-modal-menu></app-modal-menu>
    </v-navigation-drawer>
  </v-card>
</template>
<script>
import AppModalMenu from './ModalMenu.vue'

export default {
  name: 'ModalMenu',
  components: {
   AppModalMenu
  },
  data () {
    return {
      items: [
        { title: 'Home', icon: 'mdi-view-dashboard' },
        { title: 'Photos', icon: 'mdi-image' },
        { title: 'About', icon: 'mdi-help-box' }
      ],
      right: null
    }
  }
}
</script>
