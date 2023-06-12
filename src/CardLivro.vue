<script setup>
import MButton 
import{adicionarAoCarrinho, removerItemCarrinho, }
</script>
<template>
  <div class="card-livro" v-for="livro in livros" :key="livro.id">
        <div class="card-info-livro">
          <div class="wrap-livro">
            <img :src="livro.img" alt="Capa do livro" class="capa-livro" />
          </div>
          <p class="titulo-livro">{{ livro.title }}</p>
          <p class="autor-livro">{{ livro.author }}</p>
          <p class="preco-livro">{{ formatarPreco(livro.price) }}</p>
        </div>
        <div class="card-buttons-livros">
          <button @click="adicionarAoCarrinho(livro)">Adicionar ao carrinho</button>
        </div>
      </div>
</template>

<style scoped>
.detalhes-livro {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.detalhes-livro p {
  margin: 0;
}
.detalhes-livro div {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.detalhes-livro input[type='number'] {
  width: 50px;
  text-align: center;
  border: none;
  border-bottom: 1px solid black;
  background-color: transparent;
  margin-left: 10px;
}

.detalhes-livro button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: black;
  padding: 0;
  margin: 0;
}

.info-livro-preco {
  margin-left: auto;
}
.icon-capa-livro {
  width: 30px;
  margin-right: 10px;
}
</style>