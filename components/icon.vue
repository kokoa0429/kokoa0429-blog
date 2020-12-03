<template>
  <a v-if="link" :href="link" target="_blank" style="width: 100px">
    <img width="100px" :src="type + '_icon.svg'" />
  </a>
  <img v-else width="100px" :src="type + '_icon.svg'" />
</template>

<script>
export default {
  name: 'Icon',
  props: {
    type: {
      type: String,
      default: null,
    },
    link: {
      type: String,
      default: null,
    },
  },
}
</script>

<style scoped></style>
