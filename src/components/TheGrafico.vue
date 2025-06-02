<template>
  <div class="container-grafico">
    <div class="pie-chart"></div>

    <div class="legend">
      <div class="legend-item">
        <div class="color-box alimentacao"></div> Alimentação (30%)
      </div>
      <div class="legend-item">
        <div class="color-box transporte"></div> Transporte (25%)
      </div>
      <div class="legend-item">
        <div class="color-box lazer"></div> Lazer (20%)
      </div>
      <div class="legend-item">
        <div class="color-box moradia"></div> Moradia (25%)
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheGrafico'
}
</script>

<style scoped>
.container-grafico {
  display: flex;
  flex-direction: row;
  width: 500px;
  background-color: #ccc;
  margin: 30px;
  border-radius: 15px;
  padding: 20px;
}

.pie-chart {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  background: conic-gradient(
    #4caf50 0% 30%,   
    #2196f3 30% 55%,   
    #ff9800 55% 75%,   
    #f44336 75% 100%
  );
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  flex-shrink: 0; 
}

.legend {
  display: flex;
  flex-direction: column;
  gap: 12px;
  max-width: 200px;
  flex-grow: 1;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 16px;
  font-weight: 500;
  word-wrap: break-word;
}

.color-box {
  width: 20px;
  height: 20px;
  border-radius: 5px;
}

.alimentacao { background-color: #4caf50; }
.transporte  { background-color: #2196f3; }
.lazer       { background-color: #ff9800; }
.moradia     { background-color: #f44336; }

@media (max-width: 500px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  .legend {
    max-width: 100%;
    align-items: center;
  }
}
</style>
