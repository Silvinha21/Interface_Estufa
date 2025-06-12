<template>
  <div class="sensor_card">
    <img :src="icon" alt="Ícone do sensor" class="icone_sensor" />
    <div class="sensor_info">
      <h3 class="nome_sensor">{{ nome }}</h3>
      <p class="valor_sensor">{{ valor }} {{ unidade }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  nome: String,
  valor: [String, Number],
  unidade: String,
  icon: String
})
</script>

<style scoped>
.sensor_card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 140px;
  height: 160px;
  border: 2px solid #ccc;
  border-radius: 12px;
  padding: 1rem;
  background-color: #515151;
  text-align: center;
  box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
}

.icone_sensor {
  width: 40px;
  height: 40px;
  margin-bottom: 10px;
}

.nome_sensor {
  font-size: 1rem;
  font-weight: bold;
  margin-bottom: 5px;
  color: darkgray;
}

.valor_sensor {
  font-size: 1.2rem;
  color: #007bff;
}
</style>
