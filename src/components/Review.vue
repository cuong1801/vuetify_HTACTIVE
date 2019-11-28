<template>
  <div class="text-center">
    <v-rating v-model="rating"></v-rating>
    <p>Ya???</p>
  </div>
</template>
<script>
export default {
  data: () => ({
    rating: 3
  })
}
</script>
