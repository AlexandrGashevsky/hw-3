<script setup></script>

<template>
  <input
    type="number"
    v-bind:value="name"
    onkeydown="return false"
    onpaste="return false;"
    ondrop="return false;"
    
    @input="$emit( 'inputNumber' , $event.target.value)"
  />
</template>

<script>
export default {
  props: ["name"],
  data() {
    return {};
  },
};
</script>

<style>
input {
  width: 40px;
}
</style>
