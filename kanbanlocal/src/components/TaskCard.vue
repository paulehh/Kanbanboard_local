<template>
  <a class="task-card">
    <div class="task-details">
      <h3>{{ card.title }}</h3>
      <p>{{ card.description }}</p>

    </div>
  </a>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.task-card {
  background-color: var(--ds-surface-raised,#fff);
  border-radius: 3px;
  box-shadow: var(--ds-shadow-raised,0 1px 1px #091e4240,0 0 1px #091e424f);
  color: var(--ds-text,#172b4d);
  cursor: pointer;
  display: block;
  margin-bottom: 8px;
  max-width: 300px;
  min-height: 20px;
  position: relative;
  scroll-margin: 8px;
  z-index: 0;
  flex-shrink: 0;
}

.task-details {
  overflow: hidden;
  padding: 8px 8px 4px 12px;
  position: relative;
  z-index: 10;
  max-height: 100%;
}
</style>

  