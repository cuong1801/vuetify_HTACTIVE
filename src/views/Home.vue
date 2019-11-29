<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <demo></demo>
  </div>
</template>

<script>
import Demo from "@/components/Demo.vue";

export default {
  name: "home",
  components: {
    Demo
  }
};
</script>
