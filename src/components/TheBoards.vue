<template>
  <div class="boards container">
    <div class="board" v-for="(board, index) in boards" :key="index">
      <h3>{{ board.title }}</h3>
        <form @submit.prevent="addTask(index)">
          <label for="TaskInput">Nova Tarefa:</label>
            <input type="text" v-model="newTask" id="TaskInput" required>
          <button type="submit">Adicionar Tarefa</button>
        </form>
      <ul>
        <li v-for="(task, taskIndex) in board.tasks" :key="taskIndex">
          {{ task }}
          <button @click="removeTask(index, taskIndex)">Remover</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      boards: [
        { title: 'Para Fazer', tasks: [] },
        { title: 'Fazendo', tasks: [] },
        { title: 'Feito', tasks: [] }
      ],
      newTask: ''
    };
  },
  methods: {
    addTask(index) {
      if (this.newTask.trim() !== '') {
        this.boards[index].tasks.push(this.newTask);
        this.newTask = '';
      }
    },
    removeTask(boardIndex, taskIndex) {
      this.boards[boardIndex].tasks.splice(taskIndex, 1);
    }
  }
};
</script>

<style scoped>
.boards {
  display: flex;
  justify-content: space-around;
}

.board {
  flex: 1;
  border: 1px solid rgb(255, 140, 0);
  padding: 100px;
  margin: 10px;
  height: 850px;
}

.board li {
  list-style-type: none;
}

button {
  margin: 8px;
}
</style>