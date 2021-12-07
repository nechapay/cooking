<template>
  <div class="app-container fill">
    <menu-box title="завтрак" />
    <menu-box title="обед" />
    <menu-box title="ужин" />
  </div>
</template>

<script>
import MenuBox from './components/MenuBox.vue'
export default {
  name: 'App',
  components: { MenuBox }
}
</script>
    MenuBox

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.app-container {
  display: flex;
  position: fixed;
  top: 0;
  left: 0;
  background: #ccc;
}

.fill {
  width: 100%;
  height: 100%;
}
</style>
