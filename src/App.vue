<template>
    <div id="app">
        <Files :items="items" />
    </div>
</template>

<script>
  import Files from './components/Files';

  export default {
    name: 'app',
    components: { Files },
    data() {
      return {
        text: 'empty',
        items: [
          { preview: 'preview 1', name: 'name 1' },
          { preview: 'preview 2', name: 'name 2' }
        ]
      };
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
