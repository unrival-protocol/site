<template>
  <div class="tree-view">
    <li class="list">
    <ul id="demo">
      <tree-item
        class="item"
        :item="treeData"
        ></tree-item>
      </ul>
  </li>
  </div>

</template>

<script>
  import treeData from '../../tree-data.json'
  // import TreeItem from './TreeItem'

  export default {
    name: 'TreeView',
    components: {
    //  TreeItem
    },
    data() {
      return {
        treeData: treeData
      }
    }
  
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
  font-family: Menlo, Consolas, monospace;

  height: 200px;
  padding: 3vw;
  padding-top: 1vw;
  font-size: 40px;
  color: rgb(239, 237, 244);}
li {
  list-style-type: none;
}
.item {
  cursor: pointer;
}
.bold {
  font-weight: bold;
}
ul {
  padding-left: 1em;
  line-height: 1.5em;
  list-style-type: dot;
}
.list-enter-active,
.list-leave-active {
  transition: all 1s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

</style>
