<script setup>

import ListagemLivros from '@/components/ListagemLivro.vue'
import MeuCarrinho from '@/components/MeuCarrinho.vue'

</script>
<template>
  <h1>Minha livraria</h1>
  <div class="container-geral">
        <Listagem-Livros />
        <meu-carrinho />
      </div>
     
</template>

<style scoped>

.container-geral {
  display: grid;
  grid-template-columns: 3fr 1fr;
}


.carrinho {
  /* min-width: 20%; */
}

.card-livro {
  margin: 5px 10px;
  padding: 10px;
  background-color: beige;
  border-radius: 10px;
  width: 180px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
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
}

.card-livro .titulo-livro {
  font-weight: bold;
  margin-bottom: 5px;
}
</style>
