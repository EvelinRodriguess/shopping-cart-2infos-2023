<script setup>
import  MeuCarrinho from '@/components/MeuCarrinho.vue'
import  ListagemLivros from '@/components/ListagemLivro.vue'

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
</style>
