<template>
    <div id="app">
        <ul>
            <Item :key="index"
                  v-bind="item"
                  v-for="(item, index) in items"
            />
        </ul>
    </div>
</template>

<script>
  import Item from './components/File';

  export default {
    name: 'app',
    components: { Item },
    data() {
      return {
        text: 'empty',
        items: [
          { preview: 'preview 1', name: 'name 1' },
          { preview: 'preview 2', name: 'name 2' }
        ]
      };
    },
    methods: {
      onAddText() {
        this.items.push(this.text);
      },
      onDeleteText(index) {
        this.items.splice(index, 1);
      }
    }
  };
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
