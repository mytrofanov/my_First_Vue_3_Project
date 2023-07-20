<template>
  <button
    class="custom-button"
  >
    <slot></slot> <!--like children in React-->
  </button>
</template>

<script>
export default {
  name: 'custom-button'
};
</script>

<style scoped>
.custom-button{
  padding: 8px 16px;
  background: none;
  color: olivedrab;
  border: 1px solid olivedrab;
}
</style>
