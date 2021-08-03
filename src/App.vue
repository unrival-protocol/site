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
</style>
