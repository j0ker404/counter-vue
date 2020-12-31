<template>
  <div class="btn-row">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Row",
};
</script>

<style scoped>
.btn-row {
  display: flex;
  justify-content: center;
}
</style>
