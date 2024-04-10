<template>
    <div class="container">
      <div class="board" v-for="(board, index) in boards" :key="index">
        <h2>{{ board.title }}</h2>
        <ul>
          <li v-for="(item, itemIndex) in board.items" :key="itemIndex">{{ item }}</li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        boards: [
          {
            title: "Fazer",
            items: ["Item 1", "Item 2", "Item 3"]
          },
          {
            title: "Fazendo",
            items: ["Item 4", "Item 5", "Item 6"]
          },
          {
            title: "Feito",
            items: ["Item 7", "Item 8", "Item 9"]
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .container {
    display: flex;
    justify-content: space-between;
  }
  
  .board {
    flex: 1;
    margin: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  @media screen and (max-width: 768px) {
    .board-container {
      flex-direction: column;
    }
  }
  </style>