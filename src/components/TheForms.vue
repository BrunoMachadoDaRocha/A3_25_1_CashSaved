<template>
  <div v-show="visivel" class="card">
    <h5 class="card-title">Nova Categoria</h5>
    <form @submit.prevent="salvarCategoria">
      <div class="form-group">
        <label for="nomeCategoria">Nome</label>
        <q-input
          outlined
          color="black"
          v-model="categoria.nome"
          label="Digite o nome da categoria"
          :dense="dense"
          class="input-quasar"
        />
      </div>

      <div class="form-group">
        <label for="valor">Valor R$</label>
        <input
          type="number"
          id="valor"
          v-model="categoria.valor"
          placeholder="Digite Valor"
        />
      </div>

      <div class="form-group">
        <label for="tipoCategoria">Tipo</label>
        <select id="tipoCategoria" v-model="categoria.tipo">
          <option value="entrada">Entrada</option>
          <option value="saida">Saída</option>
        </select>
      </div>

      <div class="form-group">
        <label for="corCategoria">Cor</label>
        <input
          type="color"
          id="corCategoria"
          v-model="categoria.cor"
          title="Escolha uma cor"
        />
      </div>

      <div class="form-group">
        <label for="iconeCategoria">Ícone</label>
        <select id="iconeCategoria" v-model="categoria.icone">
          <option value="bi-cart">🛒 Carrinho</option>
          <option value="bi-house">🏠 Casa</option>
          <option value="bi-car-front">🚗 Carro</option>
          <option value="bi-briefcase">💼 Trabalho</option>
          <option value="bi-x-circle">Nenhum</option>
        </select>
      </div>

      <q-btn push color="primary" label="Salvar" @click="salvarCategoria" />
    </form>
  </div>

  <table class="table table-dark table-striped">
    <thead>
      <tr>
        <th>Nome</th>
        <th>Valor</th>
        <th>Tipo</th>
        <th>Ícone</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(cat, index) in categorias" :key="index">
        <td>{{ cat.nome }}</td>
        <td>R$ {{ parseFloat(cat.valor).toFixed(2) }}</td>
        <td>{{ cat.tipo }}</td>
        <td>
          <i :class="cat.icone" :style="{ color: cat.cor, fontSize: '1.5rem' }"></i>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: "TheForms",
  data() {
    return {
      visivel: true,
      categoria: {
        nome: "",
        valor: "",
        tipo: "entrada",
        cor: "#000000",
        icone: "bi-cart",
      },
      categorias: [], 
    };
  },
  methods: {
    salvarCategoria() {

      if (this.categoria.valor == '') {
        alert('Digite um valor')
      } else {
        this.categorias.push({ ...this.categoria });

        this.categoria = {
          nome: "",
          valor: "",
          tipo: "entrada",
          cor: "#000000",
          icone: "bi-cart",
        };
      }
      
    },
  },
};
</script>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 8px;
  padding: 20px;
  max-width: 500px;
  margin: auto;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.card-title {
  font-size: 20px;
  margin-bottom: 20px;
  color: #333;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 6px;
  font-weight: bold;
}

input[type="text"],
input[type="number"],
textarea,
select,
input[type="color"] {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

.input-quasar {
  width: 100%;
  padding: 8px;
  border-radius: 4px;
  box-sizing: border-box;
  border-color: #000;
}

textarea {
  resize: vertical;
}

#valor {
  color: black;
}

table {
  margin-top: 50px !important;
  width: 90%;
  text-align: center;
  margin: auto;
}
</style>
