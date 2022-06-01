<script setup></script>

<template>
  <select id="signs" name="chose-signs">
    <option value="plus">+</option>
    <option value="minus">-</option>
    <option value="division">/</option>
    <option value="multiplication">*</option>
  </select>
</template>

<script>
export default {
  props: ["name"],
  data() {
    return {};
  },
};
</script>

<style></style>
