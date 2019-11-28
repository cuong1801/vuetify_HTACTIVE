<template>

  <v-card class="d-inline-block "  style="margin-right:12px; margin-top:12px"   >
    <v-container>
      <v-row justify="space-between">
        <v-col cols="auto">
          <v-img
            height="200"
            width="200"
            :src="srcs"
          ></v-img>
         
        </v-col>

        <v-col
          cols="auto"
          class="text-center pl-0"
        >
          <v-row
            class="flex-column ma-0 fill-height"
            justify="center"
          >
            <v-col class="px-0">
              <v-btn icon>
                <v-icon>mdi-heart</v-icon>
              </v-btn>
            </v-col>

            <v-col class="px-0">
              <v-btn icon>
               <app-detail-card :srcs="srcs"></app-detail-card>
              </v-btn>
            </v-col>

            <v-col class="px-0">
              <v-btn icon>
                <v-icon>mdi-share-variant</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>
<script>
import AppDetailCard from './DetailCard.vue'
export default {
  name: 'DetailCard',
  components: {
    AppDetailCard
  },
  props: ['srcs'],

    data() {
        return {
          
        }
    },
}
</script>

