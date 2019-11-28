<template>

  <v-card class="d-inline-block " style="margin-top:12px" >
      
    <v-container >
      <v-row justify="space-between">
        <v-col cols="auto">
          <v-img
            height="200"
            width="100"
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
             <app-detail-card :srcs="srcs"></app-detail-card>
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
  props: ['srcs'],
   name: 'DetailCard',
  components: {
    AppDetailCard
  },

    data() {
        return {
          
        }
    },
}
</script>

