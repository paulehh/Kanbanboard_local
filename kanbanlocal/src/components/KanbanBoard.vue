<template>
  <div id="board">
    <KanbanColumn v-for="column in columns" :key="column.id" :column="column" />
  </div>
</template>

<script>
import KanbanColumn from '@/components/KanbanColumn.vue'; // Stellen Sie sicher, dass der Pfad korrekt ist

export default {
  name: 'KanbanBoard',
  components: {
    KanbanColumn,
  },
  data() {
    return {
      columns: [
        {
          id: 1,
          name: 'To Do',
          cards: [
            { id: 1, title: 'Karte 1', description: 'Beschreibung für Karte 1' },
            { id: 2, title: 'Karte 2', description: 'Beschreibung für Karte 2' },
            // Fügen Sie weitere Karten hier hinzu
          ],
        },
        {
          id: 2,
          name: 'In Progress',
          cards: [
            { id: 3, title: 'Karte 3', description: 'Beschreibung für Karte 3' },
            // Fügen Sie weitere Karten hier hinzu
          ],
        },
        // Fügen Sie weitere Spalten hier hinzu
      ],
    };
  },
};
</script>

<style scoped>
.kanban-board {
  display: flex;
  height: 100%;
}

#board {
  bottom: 0;
left: 0;
margin-bottom: 8px;
overflow-x: auto;
overflow-y: hidden;
padding-bottom: 8px;
position: absolute;
right: 0;
scrollbar-color: #fff6 #00000026;
scrollbar-width: auto;
top: 0;
-webkit-user-select: none;
user-select: none;
white-space: nowrap;
}
</style>
