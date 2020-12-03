<template>
  <div class="center">
    <h1>kokoa0429</h1>
    <slideshow :images="['icon1', 'icon2', 'icon3']"></slideshow>
    <Icon
      :type="'twitter'"
      :link="'https://twitter.com/love_kobato_all'"
    ></Icon>
    <Icon :type="'github'" :link="'https://github.com/kokoa0429'"></Icon>
  </div>
</template>
<script>
import Slideshow from '~/components/slideshow'
import Icon from '~/components/icon'
export default {
  components: { Slideshow, Icon },
}
</script>
<style scoped>
.center {
  text-align: center;
}
</style>
