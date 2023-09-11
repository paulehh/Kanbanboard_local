<template>
    <h1>Willkommen zum Kanban Board</h1>
    <p>Starten das Tool in dem du eine neue Datenbank erstellst oder eine vorhandene auswählst.</p>
    <div class="bt-container-row bt-container-m-column">
        <button @click="createNewDatabase">Neue Datenbank</button>
        <button @click="openExistingDatabase">Vorhandene Datenbank</button>
    </div>

</template>

<script>

</script>

<style scoped>
.bt-container-row {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    height: 100%;
}

@media screen and (max-width: 600px) {
    .bt-container-row {
        flex-direction: column;
    }
}

</style>

