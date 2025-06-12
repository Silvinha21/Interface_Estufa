<template>
  <div class="atuador_card">
    <img :src="icon" alt="Ícone do atuador" class="icon_atuador" />
    <div class="atuador-info">
      <h3 class="nome_atuador">{{ nome }}</h3>
      <p class="atuador_status" :class="{ ligado: ligado, desligado: !ligado }">
        {{ ligado ? 'Ligado' : 'Desligado' }}
      </p>
      <button @click="alternarEstado" class="botao_atuador">
        {{ ligado ? 'Desligar' : 'Ligar' }}
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, watchEffect, onMounted } from 'vue'

const props = defineProps({
  nome: String,
  icon: String,
  estadoInicial: Boolean
})

const emit = defineEmits(['atualizarEstado'])

const ligado = ref(props.estadoInicial)

function alternarEstado() {
  ligado.value = !ligado.value
  emit('atualizarEstado', ligado.value)
}
</script>

<style scoped>
.atuador_card {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 160px;
  height: 200px;
  border: 2px solid #ccc;
  border-radius: 12px;
  padding: 1rem;
  background-color: #515151;
  box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
  text-align: center;
}

.icon_atuador {
  width: 40px;
  height: 40px;
  margin-bottom: 10px;
}

.nome_atuador {
  font-size: 1rem;
  font-weight: bold;
  margin-bottom: 5px;
  color: darkgray;
}

.atuador_status {
  font-size: 1rem;
  margin-bottom: 10px;
}

.ligado {
  color: green;
}

.desligado {
  color: red;
}

.botao_atuador {
  padding: 0.4rem 1rem;
  font-size: 0.9rem;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background-color 0.2s;
}

.atuador-botao:hover {
  background-color: #0056b3;
}
</style>
