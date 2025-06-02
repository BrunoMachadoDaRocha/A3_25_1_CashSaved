<template>
  <div class="pie-chart"></div>

  <div class="legend">
    <div class="legend-item"><div class="color-box alimentacao"></div> Alimentação (30%)</div>
    <div class="legend-item"><div class="color-box transporte"></div> Transporte (25%)</div>
    <div class="legend-item"><div class="color-box lazer"></div> Lazer (20%)</div>
    <div class="legend-item"><div class="color-box moradia"></div> Moradia (25%)</div>
  </div>
</template>

<script>
export default {
  name: 'TheGrafico'
}
</script>


<style scoped>
.pie-chart {
  width: 400px;
  height: 400px;
  border-radius: 50%;
  background: conic-gradient(
    #4caf50 0% 30%,    /* Alimentação */
    #2196f3 30% 55%,   /* Transporte */
    #ff9800 55% 75%,   /* Lazer */
    #f44336 75% 100%   /* Moradia */
  );
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  margin: 0 auto 30px auto;
}

.legend {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 400px;
  margin: 0 auto;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 18px;
  font-weight: 600;
}

.color-box {
  width: 24px;
  height: 24px;
  border-radius: 5px;
}

.alimentacao { background-color: #4caf50; }
.transporte  { background-color: #2196f3; }
.lazer       { background-color: #ff9800; }
.moradia     { background-color: #f44336; }
</style>