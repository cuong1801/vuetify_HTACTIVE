<template>
  <div>
    <v-card-title class="text-center justify-center py-6">
      <h1 class="font-weight-bold display-3 basil--text">TASK TODAY</h1>
    </v-card-title>
    <app-calender style="padding:12px"></app-calender>
    <v-tabs v-model="tab" background-color="transparent" grow>
      <v-tab v-for="item in items" :key="item">{{ item }}</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in items" :key="item">
        <v-card>
          <v-card-text>{{ text }} {{item}}</v-card-text>
          <v-expansion-panels>
            <v-expansion-panel v-for="(item,i) in 2" :key="i">
              <v-expansion-panel-header expand-icon="mdi-menu-down">Task {{item}}</v-expansion-panel-header>
              <v-expansion-panel-content>Nội dung task {{item}}.</v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>
<script>
import AppCalender from "./Calender.vue";

export default {
  components: {
    AppCalender,
  },
  data() {
    return {
      tab: null,
      items: ["Yesterday", "Today", "Tommorow"],
      text: "task of"
    };
  }
};
</script>
<style scope>
/* Helper classes */
.basil {
  background-color: #fffbe6 !important;
}

.basil--text {
  color: #356859 !important;
}
</style>
