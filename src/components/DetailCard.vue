<template>
  <div class="text-center">
    <v-bottom-sheet v-model="sheet">
      <template v-slot:activator="{ on }">
        <v-btn color="purple" dark v-on="on">View</v-btn>
      </template>
      <v-sheet class="text-center" height="350px">
        <v-btn class="mt-6" flat color="red" @click="sheet = !sheet">close</v-btn>
        <v-row>
          <v-col cols="auto">
            <v-img height="200" width="200" :src="srcs"></v-img>
          </v-col>

          <v-col cols="auto">
            <h1>Title: {{srcs.title}}</h1>
          </v-col>
        </v-row>
      </v-sheet>
    </v-bottom-sheet>
  </div>
</template>
<script>
export default {
  props: ["srcs"],
  data: () => ({
    sheet: false
  })
};
</script>