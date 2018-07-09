<template>
  <div class="wrapper">
    <span class="title">{{ title }}</span>
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  color: #999999;
  margin: 5px 0;
}

.title {
  font-weight: 600;
}

.content {
  border-left: 1px solid #ccc;
  padding-left: 15px;
}
</style>
