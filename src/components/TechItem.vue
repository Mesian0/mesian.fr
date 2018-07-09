<template>
  <div
    class="tech gradient"
    v-if="tech.gradient">
    <img :src="require(`@/assets/techLogos/${tech.pic}`)" alt="tech">{{ tech.label }}
  </div>

  <div
    class="tech"
    :style="'color:' + tech.color"
    :class="{gradient: tech.gradient}"
    v-else>
    <img :src="require(`@/assets/techLogos/${tech.pic}`)" alt="tech">{{ tech.label }}
  </div>
</template>

<script>
export default {
  props: {
    tech: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss">
.tech {
  display: inline-flex;
  align-items: flex-start;
  height: 1em;
  font-weight: 600;
  margin: 0 5px;
  img {
    margin-right: 4px;
    height: 100%;
  }
}

.gradient {
  background: -webkit-linear-gradient(#78b5dc, #af939b);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
