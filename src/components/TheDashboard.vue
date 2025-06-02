<template>
  <div class="dashboard">
    <div class="top-section">
      <h2 class="section-title">Saldos</h2>

      <div class="saldo-container">
        <h3 class="saldo-label">Saldo Total:</h3>
        <p class="saldo-valor">R$ 10.000,00</p>
        <button class="btn-saldo">Ver Saldo</button>
      </div>
    </div>

    <div class="bottom-section">
      <!-- Conteúdo futuro (ex: gráficos, cards, etc.) -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheDashboard'
}
</script>

<style>
.dashboard {
  background-color: #2c3034;
  border-radius: 10px;
  margin: 30px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 20px; /* Reduzido para menor espaçamento */
}

.section-title {
  color: #fff;
  font-size: 24px;
  margin-bottom: 10px;
}

.saldo-container {
  text-align: center;
}

.saldo-label {
  color: #d9d9d9;
  font-size: 22px;
  font-weight: bold;
  margin-bottom: 5px;
}

.saldo-valor {
  font-size: 32px;
  font-weight: bold;
  color: #fff;
  margin: 5px 0;
}

.btn-saldo {
  margin-top: 10px;
  padding: 8px 16px;
  font-size: 15px;
  font-weight: bold;
  border: none;
  border-radius: 8px;
  background-color: #00b894;
  color: #fff;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-saldo:hover {
  background-color: #019870;
}

.bottom-section {
  /* Espaço reservado para futuro conteúdo */
}
</style>
