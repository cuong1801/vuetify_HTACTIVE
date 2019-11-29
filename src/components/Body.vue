<template>
  <v-container class="grey lighten-5">
    <div>
      <v-row no-gutters>
        <v-col cols="12" sm="8" md="12" style="max-width: 75.3333%">
          <app-left-body v-for="(item,index) in srcs" :key="index" :srcs="item"></app-left-body>
        </v-col>
        <v-col cols="6" md="4" style="max-width: 24.333333%">
          <v-list-item-title class="title">Latest On ACTIVE</v-list-item-title>
          <app-right-body v-for="(item,index) in srcs" :key="index" :srcs="item"></app-right-body>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>
<script>
import AppLeftBody from "./LeftBody.vue";
import AppRightBody from "./RightBody.vue";

export default {
  name: "Body",
  components: {
    AppLeftBody,
    AppRightBody
  },
  data() {
    return {
      srcs: [
        {
          src: "https://www.techrum.vn/chevereto/images/2017/01/14/8O4OT.jpg",
          title: "ảnh này là ảnh số 1 "
        },
        {
          src:
            "https://images.pexels.com/photos/1105218/pexels-photo-1105218.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          title: "ảnh này là ảnh số 2 "
        },
        {
          src: "http://www.techrum.vn/chevereto/images/2017/01/14/8GJB5.jpg",
          title: "ảnh này là ảnh số 3 "
        },
        {
          src: "http://www.techrum.vn/chevereto/images/2017/01/14/8GKC6.jpg",
          title: "ảnh này là ảnh số 4 "
        },
        {
          src: "http://www.techrum.vn/chevereto/images/2017/01/14/8GLfE.jpg",
          title: "ảnh này là ảnh số 5 "
        }
      ]
    };
  }
};
</script>
