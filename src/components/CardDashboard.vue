<template>
  <div class="container">
    <div class="infos-conta">
      <p id="conta">Conta Banco 1</p>
      <p id="valor" v-if="showValue">R$ {{ valor }}</p>
      <p id="valor" v-else>R$ *********</p>
    </div>
    <div class="botoes">
      <button id="button1" @click="toggleValue">
        {{ showValue ? 'Ocultar valor' : 'Mostrar valor' }}
      </button>
      <button id="button2" @click="adicionarValor">Adicionar</button>
    </div>
  </div>
</template>


<script>
export default {
  name: 'CardDashboard',

  data() {
    return {
      showValue: true,
      valor: 20,
    }
  },

  methods: {
    toggleValue() {
      this.showValue = !this.showValue;
    },
    adicionarValor() {
      let add = prompt('Qual é o valor a ser adicionado')
      this.valor += add
      document.getElementById('valor').innerText = this.valor
    },
  }

}
</script>


<style>
.container {
  background-color: #373b3e;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 15px;
  width: 100%;
  border-radius: 10px;
  padding: 5px;
}

.infos-contas {
  display: flex;
  flex-direction: column;
}

#conta {
  color: #008469;
  font-size: 20px;
  font-weight: bold;
}

#valor {
  color: #fff;
  font-size: 15px;
  text-align: center;
}

#button1 {
  color: #fff;
  background-color: #0d6efd;
  border: none;
  padding: 10px;
  border-radius: 5px;
  font-size: 15px;
  margin: 10px;
}

#button2 {
  color: #fff;
  background-color: #008469;
  border: none;
  padding: 10px;
  border-radius: 5px;
  font-size: 15px;
  margin: 10px;
}

</style>