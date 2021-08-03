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
  .html {
  background: hsla(180, 13%, 58%, 1);

  background: linear-gradient(90deg, hsla(180, 13%, 58%, 1) 0%, hsla(335, 16%, 61%, 1) 100%);

  background: -moz-linear-gradient(90deg, hsla(180, 13%, 58%, 1) 0%, hsla(335, 16%, 61%, 1) 100%);

  background: -webkit-linear-gradient(90deg, hsla(180, 13%, 58%, 1) 0%, hsla(335, 16%, 61%, 1) 100%);
  }
</style>
