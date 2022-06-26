<template>
  <!-- ideas for how to turn it into a game -->
  <!-- add minimum and subtract maximum until they are equal -->
  <h1>text calulator</h1>
  <p>Enter the equations you want solved</p>
  <form action="" @submit.prevent="createEquation">
    <input type="text" placeholder="Enter numbers" v-model="inputEquation" />
    <input type="submit" />
  </form>
</template>

<script>
export default {
  name: "StringCalculator",
  data() {
    return {
      inputEquation: "",
      inputEquationArray: [],
    };
  },
  computed() {},
  methods: {
    // Utility Methods

    createEquation() {
      this.inputEquationArray = this.inputEquation.split("");
      for (let i = 0; i < this.inputEquationArray.length; i++) {
        let equation = "";
        if (this.inputEquationArray[i] === "+") {
          for (let ii = 0; ii < i; ii++) {
            equation = equation + this.inputEquationArray[ii];
            console.log(equation);
            console.log(i);
          }
        }
        if (this.inputEquationArray[i] === "-") {
          for (let ii = 0; ii < i; ii++) {
            equation = equation + this.inputEquationArray[ii];
            console.log(equation);
            console.log(i);
          }
        }
        if (this.inputEquationArray[i] === "/") {
          for (let ii = 0; ii < i; ii++) {
            equation = equation + this.inputEquationArray[ii];
            console.log(equation);
            console.log(i);
          }
        }
        if (this.inputEquationArray[i] === "*") {
          for (let ii = 0; ii < i; ii++) {
            equation = equation + this.inputEquationArray[ii];
            console.log(equation);
            console.log(i);
          }
        }
      }
    },
  },
};
</script>