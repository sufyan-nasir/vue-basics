<template>
    <div>
      <h2>{{ message }}</h2>
      <button @click="changeMessage">Click Me</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        message: "Hello, Vue!"
      };
    },
    methods: {
      changeMessage() {
        this.message = "You clicked the button!";
      }
    }
  };
  </script>
  