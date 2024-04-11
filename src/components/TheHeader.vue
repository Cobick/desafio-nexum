<template>
    <nav class="navbar navbar-light bg-light container">
      <div class="nav">
        <h1>KANBAN - NEXUM</h1>
      </div>
      <div>
        <form class="pesquisar">
        <input class="campo" type="search" placeholder="Pesquisar" aria-label="Pesquisar">
        <button type="submit">Pesquisar</button>
        </form>
      </div>
    </nav>
</template>


<script>
 export default {
    name: 'TheHeader'
  }
</script>

<style>
.nav {
  display: block;
}

.nav h1 {
  font-family: "Bungee Spice", sans-serif;
  font-weight: 400;
  font-style: normal;
}

form {
  float: right;
}

.campo {
  border-radius: 5px;
  margin-right: 10px;
}

button {
  color: black;
  font-weight: 600;
  background-color: rgb(255, 140, 0);
}

button:hover {
  background-color: rgb(255, 221, 0);
}
</style>