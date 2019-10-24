<template>
    <ul>
        <File :key="index"
              v-bind="item"
              v-for="(item, index) in items"
        />
    </ul>
</template>

<script>
  import File from './File';

  export default {
    name: 'Files',
    components: { File },
    props: {
      items: Array
    }
  };
</script>

<style scoped>

</style>
