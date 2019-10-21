<template>
    <div id="app">
        <label for="input">Text: </label>
        <input @keypress.enter="onAddText" id="input" v-model="text" />
        <ul>
            <li @dblclick="onDeleteText(index)"
                v-bind:key="index"
                v-for="(item, index) in items"
            >
                {{ item }}
            </li>
        </ul>
    </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        text: 'empty',
        items: [
          'Item 1',
          'Item 2'
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
