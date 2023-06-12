<script setup>
import { adicionarAoCarrinho } from '@/_data/carrinho.js'

const props = defineProps({ livro: Object })

function formatarPreco(preco) {
  return 'R$ ' + preco.toFixed(2).replace('.', ',')
}
</script>

<template>
  <div class="card-livro">
    <div class="card-info-livro">
      <div class="wrap-livro">
        <img :src="props.livro.img" alt="Capa do livro" class="capa-livro" />
      </div>
      <p class="titulo-livro">{{ props.livro.title }}</p>
      <p class="autor-livro">{{ props.livro.author }}</p>
      <p class="preco-livro">{{ formatarPreco(props.livro.price) }}</p>
    </div>
    <div class="card-buttons-livros">
      <m-button @click="adicionarAoCarrinho(props.livro)" texto="Adicionar ao carrinho" />
      <m-button texto="Favoritar"/>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bruno+Ace+SC&family=Mukta&family=Press+Start+2P&display=swap');
.card-livro {
  margin: 5px 10px;
  padding: 10px;
  background-color: rgb(0, 0, 0);
  border-radius: 10px;
  width: 180px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  font-family: 'Mukta', sans-serif;
  font-size: 17px;
}

.wrap-livro {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  border-radius: 10px;
  width: 180px;
  height: 270px;
}
.capa-livro {
  width: 90%;
  max-height: 100%;
}

.card-livro p {
  margin: 0;
  color: white;
}

.card-livro .titulo-livro {
  font-weight: bold;
  margin-bottom: 5px;
  color: white;
}
</style>