<template>
    <footer class="footer container bg-light">
      <div class="container">
        <div class="row">
          <div class="col-md-6 text-md-left text-center">
            <p>&copy; 2024 Kanban - Nexum</p>
          </div>
          <div class="col-md-6 text-md-right text-center">
            <p>Desenvolvido por <span>Gabriel Valentin</span></p>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'TheFooter'
  }
  </script>
  
  <style scoped>
  .footer {
    color: black;
    padding: 20px 0;
  }
  .footer span {
    color: rgb(255, 140, 0);
  }
  </style>