<template>

  <TheHeader />
  <TheBoards />
  <TheFooter />
  
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheBoards from './components/TheBoards.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheBoards,
    TheFooter
  }
}

</script>

<style>
body {
  background-color: bisque;
}
</style>
