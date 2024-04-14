<template>
  <div class="container">
    <div class="row">
      <!-- Board 1 -->
      <div class="col-sm-4">
        <div class="card custom-board">
          <div class="card-header">
            <h3>Fazer</h3>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item" v-for="(item, index) in board1" :key="index">
              {{ item }}
              <button class="btn btn-danger btn-sm float-right" @click="deleteItem(1, index)">X</button>
            </li>
          </ul>
          <div class="card-footer">
            <input type="text" class="form-control" v-model="newItem1" placeholder="Nova Tarefa">
            <button class="btn btn-primary mt-2" @click="addItem(1)">Adicionar</button>
          </div>
        </div>
      </div>
      <!-- Board 2 -->
      <div class="col-sm-4">
        <div class="card custom-board">
          <div class="card-header">
            <h3>Fazendo</h3>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item" v-for="(item, index) in board2" :key="index">
              {{ item }}
              <button class="btn btn-danger btn-sm float-right" @click="deleteItem(2, index)">X</button>
            </li>
          </ul>
          <div class="card-footer">
            <input type="text" class="form-control" v-model="newItem2" placeholder="Nova Tarefa">
            <button class="btn btn-primary mt-2" @click="addItem(2)">Adicionar</button>
          </div>
        </div>
      </div>
      <!-- Board 3 -->
      <div class="col-sm-4">
        <div class="card custom-board">
          <div class="card-header">
            <h3>Feito</h3>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item" v-for="(item, index) in board3" :key="index">
              {{ item }}
              <button class="btn btn-danger btn-sm float-right" @click="deleteItem(3, index)">X</button>
            </li>
          </ul>
          <div class="card-footer">
            <input type="text" class="form-control" v-model="newItem3" placeholder="Nova Tarefa">
            <button class="btn btn-primary mt-2" @click="addItem(3)">Adicionar</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newItem1: '',
      newItem2: '',
      newItem3: '',
      board1: ['Estudar'],
      board2: ['Trabalhar'],
      board3: ['Correr']
    };
  },
  methods: {
    addItem(boardIndex) {
      if (boardIndex === 1 && this.newItem1.trim() !== '') {
        this.board1.push(this.newItem1);
        this.newItem1 = '';
      } else if (boardIndex === 2 && this.newItem2.trim() !== '') {
        this.board2.push(this.newItem2);
        this.newItem2 = '';
      } else if (boardIndex === 3 && this.newItem3.trim() !== '') {
        this.board3.push(this.newItem3);
        this.newItem3 = '';
      }
    },
    deleteItem(boardIndex, itemIndex) {
      if (boardIndex === 1) {
        this.board1.splice(itemIndex, 1);
      } else if (boardIndex === 2) {
        this.board2.splice(itemIndex, 1);
      } else if (boardIndex === 3) {
        this.board3.splice(itemIndex, 1);
      }
    }
  }
};
</script>

<style scoped>
.custom-board {
  margin-bottom: 20px;
  height: 800px;
  border: 2px solid rgb(255, 140, 0);
}

.btn {
  background-color: rgb(255, 140, 0);
}

.card-header h3 {
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-weight: weight;
  font-style: normal;
}
</style>