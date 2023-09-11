<script setup>
  import HeaderComponent from '@/components/HeaderComponent.vue';

</script>

<template>
  <HeaderComponent />
  <main>
    <div style="display: flex; flex-direction: row; flex: 1 1 0%; position: relative; overflow-y: auto;">
      <nav></nav>
      <div style="display: flex; flex-direction: column; flex: 1 1 0%; overflow-y: auto;">
        <div id="content">
          <router-view></router-view>
        </div>       
      </div>
    </div>
    
  </main>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
* {
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    font-family: sans-serif, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  html {
    height: 100%;
    min-height: 100vh;
    min-height: -moz-available;
    min-height: -webkit-fill-available;
    min-height: fill-available;
    width: 100vw;
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
  }
  
  body   {
      width: 100%;
      height: 100%;
      min-height: 100vh;
      min-height: -moz-available;
      min-height: -webkit-fill-available;
      min-height: fill-available;
      margin: 0;
      padding: 0;
      position: relative;
      box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
  }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  height: 100%;
}

#content {
  outline: none;
  overflow-y: auto;
  position: relative;
  flex-grow: 1;
}

main {
  position: relative;
  overflow-y: auto;
  outline: none;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

h1 {
  font-size: 2rem;
  margin: 0;
}

h2 {
  font-size: 1.5rem;
  margin: 0;
}

h3 {
  font-size: 1.25rem;
  margin: 0;
}

h4 {
  font-size: 1rem;
  margin: 0;
}



</style>
