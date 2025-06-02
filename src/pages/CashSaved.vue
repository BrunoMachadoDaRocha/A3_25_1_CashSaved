<template>
  <div>
    <TheHeader />
    <h2>Resumo Financeiro</h2>
    <TheDashboard />
  </div>
</template>

<script>
import TheHeader from '../components/TheHeader.vue'
import TheDashboard from '../components/TheDashboard.vue'

export default {
  name: 'CashSaved',
  data() {
    return {

    }
  }, 
  components: {
    TheHeader,
    TheDashboard
  }
}
</script>

<style>
h2 {
    font-weight: bold;
    color: #008469;
    font-size: 30px;
    text-align: center;
}
</style>
