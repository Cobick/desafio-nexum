<template>

  <TheHeader />
  <TheBoards />
  
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheBoards from './components/TheBoards.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheBoards
  }
}

</script>

<style>
body {
  background-color: bisque;
}
</style>
