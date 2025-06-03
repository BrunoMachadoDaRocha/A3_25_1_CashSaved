<template>
    <div>
        <the-header />
        <h2>Gerenciamento de Categorias</h2>
        <TheForms />
        <TheFooter class="pe"/>
    </div>
</template>
<script>
import TheFooter from '../components/TheFooter.vue'
import TheHeader from '../components/TheHeader.vue'
import TheForms from '../components/TheForms.vue'

export default {
  name: 'CashSaved',
  data() {
    return {

    }
  }, 
  components: {
    TheHeader,
    TheFooter,
    TheForms
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
  bottom: 0;
  width: 100%;
}
</style>