<template>
  <div id="app">
    <TreeView />
  </div>
</template>

<script>
import TreeView from './components/TreeView.vue'
import vue from 'vue'
import TreeItem from './components/TreeItem.vue'

vue.component("tree-item", TreeItem)



export default {
  name: 'App',
  components: {
    TreeView
  }
}
</script>

<style>
  body {
  color: rgb(250, 255, 248);
  background: #0052d4; /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #0052d4, #4364f7, #6fb1fc); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #0052d4, #4364f7, #6fb1fc); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  }
</style>
