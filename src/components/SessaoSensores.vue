<template>
  <section class="sessao_sensores">
    <h2>Sensores</h2>
    <div class="sensores_grid">
      <SensorCard
        nome="Temperatura Ar"
        valor="25"
        unidade="°C"
        :icon="`${iconPath}/TempAr.png`"
      />
      <SensorCard
        nome="Temperatura Água"
        valor="22"
        unidade="°C"
        :icon="`${iconPath}/TempAgua.png`"
      />
      <SensorCard
        nome="Luminosidade"
        valor="80"
        unidade="%"
        :icon="`${iconPath}/Luminosidade.png`"
      />
      <SensorCard
        nome="Umidade Ar"
        valor="60"
        unidade="%"
        :icon="`${iconPath}/Umidade.png`"
      />
    </div>
  </section>
</template>

<script setup>
import SensorCard from './SensorCard.vue'

// Caminho base para os ícones
const iconPath = '/src/components/icons'
</script>

<style scoped>
.sessao_sensores {
  margin: 2rem 0;
  padding: 1rem;
  background-color: #2d2d2d;
  border-radius: 12px;
}

.sessao_sensores h2 {
  text-align: center;
  margin-bottom: 1.5rem;
  font-size: 1.5rem;
}

.sensores_grid {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 1.5rem;
}
</style>
