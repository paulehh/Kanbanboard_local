<script setup>
import KanbanBoard from '@/components/KanbanBoard.vue';


</script>

<template>
    <div class=board-container>
        <div class="board-canvas">
        <KanbanBoard />
        </div>
    </div>

  </template>
  
  <script>
  export default {
    name: 'BoardView',
  };
  </script>

    <style scoped>
    .board-container {
        display: flex;
        flex-direction: column;
        height: 100%;
        margin-right: 0;
        position: relative;
    }
    .board-canvas {
        flex-grow: 1;
        margin-top: 12px;
        position: relative;
    }
    </style>
  