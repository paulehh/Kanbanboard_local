<template>
    <div>
      <h2>Epics</h2>
      <ul>
        <li v-for="epic in epics" :key="epic.id">
          <router-link :to="{ name: 'board', params: { id: epic.id } }">{{ epic.name }}</router-link>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        epics: [
          { id: 1, name: "Epic 1" },
          { id: 2, name: "Epic 2" }
          // ... Weitere Epics
        ]
      };
    }
  };
  </script>
  