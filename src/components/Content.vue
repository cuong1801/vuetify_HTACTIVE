<template>
  <v-carousel>
    <v-carousel-item
      v-for="(src, i) in srcs"
      :key="src"
    >
      <v-sheet

        height="100%"
        tile
      >
      <v-img
      :src="src"
      :lazy-src="src"
      aspect-ratio="1"
      class="grey lighten-2"
      height="100%"

    ></v-img>
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-3">Slide {{ i + 1 }}</div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data () {
    return {
      srcs: [
        require('../image/36639853_1779134148830111_5226755335561150464_n.jpg'),
        require('../image/36679889_1779134442163415_7136537729415774208_n.jpg'),
        require('../image/71590013_2504612046282314_6560878357880242176_n.jpg'),
        require('../image/chicago.jpg'),
        require('../image/la.jpg'),

      
      ]
    }
  }
}
</script>
