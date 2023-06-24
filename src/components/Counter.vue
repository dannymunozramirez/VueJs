<template>
  <h2>{{ customTitle }}</h2>
  <p>{{ counter }}<sup>2</sup> = {{ squareCounter }}</p>

  <div>
    <button @click="increase()">+1</button>
    <button @click="decrease()">-1</button>
  </div>
</template>
<script>
// Any property within data will be reactive
export default {
  // Here is where properties are
  props: {
    title: String,
    start: {
      type: Number,
      default: 100,
      validator(value) {
        return value > 100;
      },
    },
  },
  data() {
    return {
      counter: this.start,
    };
  },
  // Functions are called as many as need it
  methods: {
    getSquareValue() {
      return this.counter * this.counter;
    },
    increase() {
      this.counter++;
    },
    decrease() {
      this.counter--;
    },
  },
  // Computed properties are save it in cache it is call once
  computed: {
    squareCounter() {
      return this.counter * this.counter;
    },
    customTitle() {
      return this.title ? this.title : "Counter";
    },
  },
};
</script>
<style>
/* Pallet -> sort lines ascending */
button {
  background-color: #64bb87;
  border-radius: 5px;
  border: 1px solid white;
  color: white;
  cursor: pointer;
  margin: 0 5px;
  padding: 5px 15px;
  transition: 0.3s ease-in-out;
}
button:hover {
  background-color: #5aa67b;
  transition: 0.3s ease-in-out;
}
</style>
