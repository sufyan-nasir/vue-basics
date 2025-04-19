<template>
    <div>
      <h1>Hello, {{ name }} 👋</h1>
  
      <input v-model="name" placeholder="Type your name" />
  
      <p v-if="name">You typed: {{ name }}</p>
      <p v-else>Please enter your name above</p>
  
      <h2>My Todo List</h2>
      <ul>
        <li v-for="(todo, index) in todos" :key="index">
          {{ index + 1 }}. {{ todo }}
        </li>
      </ul>
  
      <input v-model="newTodo" placeholder="Add a todo" />
      <button @click="addTodo">Add</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        todos: ['Learn Vue', 'Build Project', 'Master Nuxt'],
        newTodo: ''
      };
    },
    methods: {
      addTodo() {
        if (this.newTodo.trim() !== '') {
          this.todos.push(this.newTodo);
          this.newTodo = '';
        }
      }
    }
  };
  </script>
  
  <style>
  body {
    font-family: 'Segoe UI', sans-serif;
    background: #f0f0f0;
    padding: 20px;
  }
  input {
    padding: 5px;
    margin-bottom: 10px;
    display: block;
  }
  button {
    padding: 5px 10px;
    background-color: #41b883;
    color: white;
    border: none;
    cursor: pointer;
  }
  </style>
  