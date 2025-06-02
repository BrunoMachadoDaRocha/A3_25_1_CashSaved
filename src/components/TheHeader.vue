<template>
  <header class="header">
    <div class="logo-container">
      <img src="../assets/Logo.png" alt="Logo de nossa aplicação" class="logo">
      <h2 class="title">Cash $aved</h2>
    </div>

    <nav class="navigation">
      <ul class="nav-list">
        <li><a href="#"><i class="bi bi-house-door"></i>Dashboard</a></li>
        <li><a href="#"><i class="bi bi-wallet2"></i>Contas</a></li>
        <li><a href="#"><i class="bi bi-tags"></i>Categorias</a></li>
        <li><a href="#"><i class="bi bi-flag"></i>Metas</a></li>
        <li><a href="#"><i class="bi bi-graph-up"></i>Projeções</a></li>
        <li><a href="#"><i class="bi bi-receipt"></i>Visão anual</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
}
</script>

<style>
.header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: rgb(0 132 105)
}

.logo-container {
  display: flex;
  align-items: center;
}

.logo {
  width: 70px;
  margin-right: 10px;
}

.title {
  font-size: 30px;
  font-weight: bold;
  color: #fff;
}

.navigation {
  display: flex;
}

.nav-list {
  list-style: none;
  display: flex;
  gap: 20px;
  margin: 0;
  padding: 0;
}

.nav-list li a {
  text-decoration: none;
  color: #fff;
  transition: 0.5s;
}

.nav-list li a:hover {
  color: #ccc;
  font-size: 15px;
}

i {
  color: #fff;
  padding: 9px;
}

@media (max-width: 600px) {

  header {
    display: flex;
    flex-direction: column;
  }

  .nav-list {
    flex-direction: column;
  }

}
</style>
