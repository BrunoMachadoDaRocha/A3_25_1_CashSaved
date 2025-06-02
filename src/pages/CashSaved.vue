<template>
  <div>
    <TheHeader />
    <h4>Resumo Financeiro</h4>
    <TheDashboard />
    <div class="div-graficos">
      <TheGrafico />
      <TheGrafico />
      <TheGrafico />
    </div>
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from '../components/TheHeader.vue'
import TheDashboard from '../components/TheDashboard.vue'
import TheFooter from '../components/TheFooter.vue'
import TheGrafico from '../components/TheGrafico.vue'


export default {
  name: 'CashSaved',
  data() {
    return {

    }
  }, 
  components: {
    TheHeader,
    TheDashboard,
    TheFooter,
    TheGrafico
  }
}
</script>

<style>
h4 {
    font-weight: bold;
    color: #008469;
    font-size: 30px;
    text-align: center;
    margin-top: 20px;
}

.div-graficos {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

@media (max-width: 600px) {

.div-graficos {
  display: flex;
  flex-direction: column;
}

}

</style>
