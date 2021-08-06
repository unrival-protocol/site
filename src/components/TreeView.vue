<template>
<div class="tree-view" style="display: grid; grid-template-columns: 1fr 1fr">
  <div class="left-panel">
    <li class="list">
    <ul id="demo">
      <tree-item
        class="item"
        :item="treeData"
        ></tree-item>
      </ul>
  </li>

  </div>
  <div class="right-panel">
    <img :src="image1" />
  </div>
</div>

</template>

<script>
import treeData from '../../tree-data-2.json'
import image1 from "../../assets/images/pic1.png"
import image2 from "../../assets/images/pic2.png"
import image3 from "../../assets/images/pic3.png"

// import TreeItem from './TreeItem'

export default {
    name: 'TreeView',
    components: {
        //  TreeItem
    },
    mounted () {
        console.log(this.image1)
    },
    data() {
        return {
            treeData: treeData,
            image1: image1,
            image2: image2,
            image3: image3,
            currentImage: ''

      }
    }
  
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
    font-family: Menlo, Consolas, monospace;
    
    padding: 3vw;
    padding-top: 1vw;
    font-size: 25px;
}
.comment {
    color: rgb(165, 160, 160);
    
}
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
.right-panel {
    
    height: 100%;
    padding: 0;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 10%;
}

</style>
