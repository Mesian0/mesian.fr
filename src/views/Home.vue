<template>
  <div class="home">
    <app-cv></app-cv>
  </div>
</template>

<script>
import AppCv from '@/components/AppCv'
export default {
  components: {
    AppCv
  },
  data () {
    return {
      myVar: 'toto'
    }
  }
}
</script>

<style lang="scss">
.home {
  position: relative;
  width: 100%;
  display: flex;
  align-items: center;
}
</style>
