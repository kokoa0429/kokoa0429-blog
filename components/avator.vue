<template>
  <div style="height: 350px">
    <img :src="image + '.jpg'" width="300px" style="margin: auto" />
  </div>
</template>

<script>
export default {
  name: 'Icon',
  props: {
    image: {
      type: String,
      default: null,
    },
  },
}
</script>

<style scoped></style>
