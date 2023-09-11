<template>
    <header>
      <h1>{{ title }}</h1>
      <nav>
        <ul>
          <li><router-link to="/">Startseite</router-link></li>
          <li><router-link to="/board">Kanban Board</router-link></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        title: 'Secure Kanban Board',
      };
    },
  };
  </script>
  
  <style scoped>
  header {
    background-color: #333;
    color: #fff;
    padding: 1rem;
  }
  
  h1 {
    margin: 0;
  }
  
  nav ul {
    list-style: none;
    padding: 0;
    display: flex;
  }
  
  nav li {
    margin-right: 1rem;
  }
  
  nav a {
    color: #fff;
    text-decoration: none;
  }
  </style>
  