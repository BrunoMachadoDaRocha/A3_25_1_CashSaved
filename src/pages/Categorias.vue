<template>
    <div>
        <the-header />
        <h2>Gerenciamento de Categorias</h2>
    </div>
    
</template>
<script>
import TheHeader from '../components/TheHeader.vue'
export default {
  name: 'CashSaved',
  data() {
    return {

    }
  }, 
  components: {
    TheHeader
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