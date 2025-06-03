<template>
    <div>
        <the-header />
        <h2>Gerenciamento de Categorias</h2>
        <TheFooter class="pe"/>
    </div>
</template>
<script>
import TheFooter from '../components/TheFooter.vue'
import TheHeader from '../components/TheHeader.vue'
export default {
  name: 'CashSaved',
  data() {
    return {

    }
  }, 
  components: {
    TheHeader,
    TheFooter
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
.pe {
  position: fixed;
  bottom: 0;
  width: 100%;
}
</style>