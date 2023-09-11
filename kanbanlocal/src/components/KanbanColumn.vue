//KanbanColumn.vue

<template>
  <div class="kanban-column-wrapper">
    <div class="kanban-column">
      <div class="column-header">
      <h3>{{ column.name }}</h3>
    </div>
    <div class="task-cards">
      <TaskCard v-for="card in column.cards" :key="card.id" :card="card" />
    </div>
    <div class="column-footer">
      <button class="add-task">
        <span class="add-task-text">Add Task</span>
      </button>
    </div>
    </div>
  </div>
</template>

<script>
import TaskCard from "./TaskCard.vue";

export default {
  components: { TaskCard },
  props: ["column"]
};
</script>

<style scoped>
.kanban-column-wrapper {
  box-sizing: border-box;
  display: inline-block;
  height: 100%;
  margin: 0 4px;
  scroll-margin: 8px;
  vertical-align: top;
  white-space: nowrap;
  width: 272px;
}
.kanban-column {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  max-height: 100%;
  position: relative;
  white-space: normal;
  width: 100% !important;
  background-color: #566168;
}

.column-header {
  background-color: #566168;
  color: #fff;
  text-align: center;
  padding: 10px;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}

.task-cards {
  display: flex;
  flex: 1 1 auto;
  flex-direction: column;
  gap: 7px;
  justify-content: space-between;
  margin: 0 4px;
  min-height: 0;
  overflow-x: hidden;
  overflow-y: auto;
  padding: 1px 4px 0;
  z-index: 1;
}

.column-footer {
  align-items: center;
  display: flex;
  flex-shrink: 0;
  justify-content: space-between;
  max-height: revert;
  min-height: revert;
}

.add-task {
  display: block;
  border: none;
  flex: 1 0 auto;
  margin: 8px 8px 8px 8px;
  padding: 4px 8px 4px 6px;
  position: relative;
  text-decoration: none;
  cursor: pointer;
}
</style>

  