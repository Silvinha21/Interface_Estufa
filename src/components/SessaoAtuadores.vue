<template>
  <section class="sessao_atuadores">
    <h2>Atuadores</h2>
    <div class="atuadores_grid">
      <AtuadorCard
        nome="Bomba d'Água"
        :icon="`${iconPath}/BombaLigada.png`"
        :estadoInicial="false"
        @atualizarEstado="estado => console.log('Bomba:', estado)"
      />
      <AtuadorCard
        nome="Ventilação"
        :icon="`${iconPath}/VentLigada.png`"
        :estadoInicial="true"
        @atualizarEstado="estado => console.log('Ventilação:', estado)"
      />
      <AtuadorCard
        nome="Iluminação"
        :icon="`${iconPath}/IlumiLigada.png`"
        :estadoInicial="true"
        @atualizarEstado="estado => console.log('Iluminação:', estado)"
      />
    </div>
  </section>
</template>

<script setup>
import AtuadorCard from './AtuadorCard.vue'

const iconPath = '/src/components/icons'
</script>

<style scoped>
.sessao_atuadores {
  margin: 2rem 0;
  padding: 1rem;
  background-color: #2d2d2d;
  border-radius: 12px;
}

.sessao_atuadores h2 {
  text-align: center;
  margin-bottom: 1.5rem;
  font-size: 1.5rem;
}

.atuadores_grid {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 1.5rem;
}
</style>
