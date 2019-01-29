<template>
  <div class="home">
    <Draggable />
  </div>
</template>

<script>
// @ is an alias to /src
import Draggable from '@/components/Draggable.vue'

export default {
  name: 'home',
  components: {
    Draggable
  }
}
</script>

<style scoped>
.home {
  margin: 40px;
}
</style>