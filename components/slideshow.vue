<template>
  <div>
    <Avator :image="nowImage"></Avator>
    <div class="mb-s">
      <button type="button" @click="prev()">＜</button>
      <button type="button" @click="next()">＞</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SlideShow',
  props: {
    images: {
      type: Array,
      default: null,
    },
  },
  data() {
    return {
      nowImage: null,
      imageIndex: 0,
    }
  },
  created() {
    this.nowImage = this.images[0]
  },
  methods: {
    next() {
      this.imageIndex =
        this.imageIndex === this.images.length - 1
          ? (this.imageIndex = 0)
          : (this.imageIndex += 1)
      this.nowImage = this.images[this.imageIndex]
    },
    prev() {
      this.imageIndex =
        this.imageIndex === 0
          ? (this.imageIndex = this.images.length - 1)
          : (this.imageIndex -= 1)
      this.nowImage = this.images[this.imageIndex]
    },
  },
}
</script>

<style scoped>
.mb-s {
  margin-bottom: 30px;
}
</style>
