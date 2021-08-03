<template>
<li class="list">
        <div
          :class="{bold: isFolder}"
          @click="toggle"
          @dblclick="makeFolder">
          <span v-if="item.link" :class="item.class">
          <a :href="item.link">{{ item.name }}</a>
          </span>
          <span v-else  :class="item.class">
          {{ item.name }}
          </span>

          <span v-if="isFolder">[{{ isOpen ? '-' : '+' }}]</span>
        </div>
        <ul v-show="isOpen" v-if="isFolder">
          <tree-item
            class="item"
            v-for="(child, index) in item.children"
            :key="index"
            :item="child"
            @make-folder="$emit('make-folder', $event)"
            @add-item="$emit('add-item', $event)"
          ></tree-item>
        </ul>
      </li>
</template>
<script>
  export default {
        template: "#item-template",      
        props: {
          item: Object,
        },
        
        data: function () {
          return {
            isOpen: false
          };
        },
        computed: {
          isFolder: function () {
            return this.item.children && this.item.children.length;
          }
        },
        methods: {
          toggle: function () {
            if (this.isFolder) {
              this.isOpen = !this.isOpen;
            }
          },
          makeFolder: function () {
            if (!this.isFolder) {
              this.$emit("make-folder", this.item);
              this.isOpen = true;
            }
          }
        }
  }


</script>
<style>
  .definition {
  font-style: italic
  }
</style>
