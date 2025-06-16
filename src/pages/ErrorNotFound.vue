<template>
  <div class="flex">
    <h1 class="titulo_erro">Ops.. Página não encontrada <br> <span>ERROR 404</span></h1>
    <img src="../assets/Logo.png" alt="Logo">
    <RouterLink to="/" class="btn_voltar"><i class="bi bi-house-door"></i>Voltar</RouterLink>
  </div>
</template>

<script setup>

</script>

<style scoped>

.flex {
  display: flex;
  flex-direction: column;
}

span {
  color: #ff0000;
  font-size: 75px;
}

.titulo_erro {
  font-size: 30px;
  color: #fff;
  font-weight: bold;
  text-align: center;
  margin: 30px;
}

img {
  width: 150px;
  margin: auto;
}

.btn_voltar {
  padding: 30px;
  background-color: #008469;
  width: 200px;
  border-radius: 20px;
  text-align: center;
  margin: auto;
  font-weight: bold;
  text-decoration: none;
  font-size: 20px;
  color: #fff;
  transition: 0.5s;
}

i {
  transition: 0.5s;
}

.btn_voltar:hover {
  background-color: #fff;
  color: #008469;

    i {
      color: #008469;
    }
}
</style>
