<template>
    <div class="root">
        <img :alt="preview" :src="preview" />
        <h3>{{name}}</h3>
    </div>
</template>

<script>
  export default {
    name: 'File',
    props: {
      preview: String,
      name: String
    }
  };
</script>

<style scoped>
    .root {
        background-color: wheat;
    }
</style>
