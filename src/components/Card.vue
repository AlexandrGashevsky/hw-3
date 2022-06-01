<script setup>
import InputComponent from "./InputComponent.vue";
import SignComponent from "./SignComponent.vue";
</script>

<template>
  <div class="card">
    <div class="top">
      <InputComponent
        v-bind:value="firstNumber"
        v-on:input="(newFiltersState) => (firstNumber = newFiltersState.data)"
      />
      <SignComponent
        v-bind:value="sign"
        v-on:change="(newFiltersState) => (sign = newFiltersState.target.value)"
      />
      <InputComponent
        v-bind:value="secondNumber"
        v-on:input="(newFiltersState) => (secondNumber = newFiltersState.data)"
      />
    </div>
    <p>Result: {{ count(firstNumber, secondNumber, sign) }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstNumber: 0,
      secondNumber: 0,
      sign: "plus",
    };
  },
  methods: {
    count(first, second, symbol) {
      switch (symbol) {
        case "plus":
          return parseInt(first) + parseInt(second);
          break;
        case "minus":
          return parseInt(first) - parseInt(second);
          break;
        case "division":
          return parseInt(first) / parseInt(second);
          break;
        case "multiplication":
          return parseInt(first) * parseInt(second);
          break;
      }
    },
  },
};
</script>

<style>
@import "@/scss/card.scss";
</style>
