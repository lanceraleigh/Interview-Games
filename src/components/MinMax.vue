<template>
  <!-- ideas for how to turn it into a game -->
  <!-- add minimum and subtract maximum until they are equal -->
  <h1>Min Max Calculator</h1>
  <p>Enter numbers one by one to create array</p>
  <form action="" @submit.prevent="createArray">
    <input type="text" placeholder="Enter numbers" v-model="inputNumber" />
    <input type="submit" />
  </form>
  <p>The array is as follows:</p>
  <p>{{ inputArray.join(" , ") }}</p>
  <p>The Smallest number is:</p>
  <p>{{ minValue }}</p>
  <p>The Largest number is:</p>
  <p>{{ maxValue }}</p>
</template>

<script>
export default {
  name: "MinMax",
  data() {
    return {
      inputNumber: "",
      inputArray: [],
      minValue: "",
      maxValue: "",
    };
  },
  computed() {},
  methods: {
    // Utility Methods
    findMin(arr) {
      for (let i = 0; i < arr.length; i++) {
        if (arr[i] < parseInt(this.minValue, 10)) {
          this.minValue = arr[i];
        }
      }
    },
    findMax(arr) {
      console.log(arr.length);
      for (let i = 0; i < arr.length; i++) {
        if (arr[i] > parseInt(this.maxValue, 10)) {
          this.maxValue = arr[i];
        }
      }
    },
    createArray() {
      this.inputArray.push(parseInt(this.inputNumber, 10));
      this.minValue = this.inputArray[0];
      this.maxValue = this.inputArray[0];
      this.findMin(this.inputArray);
      this.findMax(this.inputArray);
    },
  },
};
</script>