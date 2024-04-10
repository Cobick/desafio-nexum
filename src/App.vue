<template>

  <TheHeader />
  <TheBoard />
  
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheBoard from './components/TheBoard.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheBoard
  }
}

</script>

<style>
body {
  background-color: bisque;
}
</style>
