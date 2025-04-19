<template>
    <div>
      <h1>{{ message }}</h1>
      <h2> You click {{ count }} time{{ count != 1 ? 's' : '' }}</h2>
      <button @click="clickMeUp">Click Me</button>
    </div>
  </template>
  
  <script>
  export default {
    data(){
      return {
        message: "Hi there!",
        count: 0
      };
    },
    methods : {
      clickMeUp(){
        this.message = "You clicked so hard...!!!",
        this.count++
      }
    }
  };
  </script>