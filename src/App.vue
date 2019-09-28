<template>
  <div id="app">
    <button @click="isCompany = !isCompany">Toggle prop</button>
    <good-old-way :is-company="isCompany" />
    <component-way :is-company="isCompany" />
    <dynamic-import-way :is-company="isCompany" />
  </div>
</template>

<script>
import GoodOldWay from './GoodOldWay'
import ComponentWay from './ComponentWay'
import DynamicImportWay from './DynamicImportWay'

export default {
  name: 'App',
  components: {
    GoodOldWay,
    ComponentWay,
    DynamicImportWay,
  },
  data() {
    return {
      isCompany: true,
    }
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}

h1 {
  margin-top: 40px;
}

button {
  margin-bottom: 20px;
  padding: 10px;
}
</style>
