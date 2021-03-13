<template>
  <button @click="test()">IPCrender test</button>
</template>

<script>
import isElectron from 'is-electron';

export default {
  name: 'App',
  methods: {
    test() {
      console.log("Electron?")
      if (isElectron()) {
        console.log("Ja, Electron!")

        console.log(window.ipcRenderer);
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
