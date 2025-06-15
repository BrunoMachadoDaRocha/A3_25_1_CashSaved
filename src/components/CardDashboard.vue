<template>
  <div class="container">
    <div class="infos-conta">
      <p id="conta">Conta Banco {{ conta }}</p>
      <p id="valor" v-if="showValue">R$ {{ valorInterno }}</p>
      <p id="valor" v-else>R$ *********</p>
    </div>

    <div class="botoes">
      <button id="button1" @click="toggleValue">
        {{ showValue ? 'Ocultar valor' : 'Mostrar valor' }}
      </button>
      <button id="button2" @click="mostrarInput = !mostrarInput">
        {{ mostrarInput ? 'Cancelar' : 'Adicionar' }}
      </button>
    </div>

    <div v-if="mostrarInput" class="input-container">
      <input
        type="number"
        v-model.number="novoValor"
        placeholder="Digite o valor a adicionar"
        class="input-valor"
      />
      <button id="button3" @click="confirmarAdicao">Confirmar</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardDashboard',

  props: {
    conta: {
      type: String,
      required: true
    },
    valor: {
      type: Number,
      required: true
    },
  },

  data() {
    return {
      showValue: false,
      valorInterno: this.valor,
      mostrarInput: false,
      novoValor: null
    }
  },

  watch: {
    valor(newVal) {
      this.valorInterno = newVal;
    }
  },

  methods: {
    toggleValue() {
      this.showValue = !this.showValue;
    },
    confirmarAdicao() {
      if (!isNaN(this.novoValor) && this.novoValor !== null) {
        this.valorInterno += this.novoValor;
        this.$emit('update-valor', this.valorInterno);
        this.novoValor = null;
        this.mostrarInput = false;
      } else {
        alert('Digite um valor válido.');
      }
    }
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

.infos-conta {
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

#button1,
#button2,
#button3 {
  color: #fff;
  border: none;
  padding: 10px;
  border-radius: 5px;
  font-size: 15px;
  margin: 10px;
}

#button1 {
  background-color: #0d6efd;
}

#button2 {
  background-color: #008469;
}

#button3 {
  background-color: #6c757d;
  transition: 0.5s;
}

#button3:hover {
  color: #6c757d;
  background-color: #FFF;
}

.input-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 10px;
}

.input-valor {
  padding: 8px;
  font-size: 14px;
  border-radius: 5px;
  border: 1px solid #ccc;
  margin-bottom: 8px;
}
</style>
