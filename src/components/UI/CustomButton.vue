<template>
  <button
    class="custom-button"
  >
    <slot></slot> <!--like children in React-->
  </button>
</template>

<script>
export default {

};
</script>

<style scoped>
.custom-button{
  margin-top: 16px;
  padding: 8px 16px;
  background: none;
  color: olivedrab;
  border: 1px solid olivedrab;
}
</style>
