<template>
  <!-- ToDo List: -->
  <!-- Reverse a string -->
  <!-- Reverse a sentence ("bob likes dogs" -> "dogs likes bob") -->
  <!-- Calculate a remainder (given a numerator and denominator) -->
  <!-- Return distinct values from a list including duplicates (i.e. "1 3 5 3 7 3 1 1 5" -> "1 3 5 7") -->
  <!-- Return distinct values and their counts (i.e. the list above becomes "1(3) 3(3) 5(2) 7(1)") -->
  <!-- Given a string of expressions (only variables, +, and -) and a set of variable/value pairs (i.e. a=1, b=7, c=3, d=14) return the result of the expression ("a + b+c -d" would be -3). -->
  <StringCalculator v-if="displayStringCalculator" />
  <!-- Find the minimum value in a list -->
  <!-- Find the maximum value in a list -->
  <!-- Done -->
  <MinMax v-if="displayMinMax" />
  <!-- FizzBuzz Game -->
  <!-- Done -->
  <FizzBuzz v-if="displayFizzBuzz" />
</template>

<script>
import FizzBuzzVue from "./components/FizzBuzz.vue";
import MinMaxVue from "./components/MinMax.vue";
import StringCalculatorVue from "./components/StringCalculator.vue";
export default {
  name: "App",
  data() {
    return {
      displayStringCalculator: true,
      displayMinMax: false,
      displayFizzBuzz: false,
    };
  },
  components: {
    FizzBuzz: FizzBuzzVue,
    MinMax: MinMaxVue,
    StringCalculator: StringCalculatorVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #333;
  color: #8e9e31;
  margin: 0;
  padding: 1rem;
}
</style>
