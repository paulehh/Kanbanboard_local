<script setup>
import StartDialog from '@/components/StartDialog.vue';
import { ref } from 'vue'

const flexId = ref('flex-container')

</script>

<template>
  <div :id="flexId">
    <StartDialog />
  </div>
</template>

<script>

export default {
  components: {
    StartDialog,
  },
};
</script>

<style scoped>

#flex-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
}

</style>
