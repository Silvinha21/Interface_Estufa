<template>
  <div class="container">
    <header>
        <h1>Estufa Automatizada Indoor</h1>
    </header>

    <main>
        <SessaoSensores />
        <SessaoAtuadores />
    </main>
  </div>
</template>

<script setup>
import SessaoSensores from './components/SessaoSensores.vue';
import SessaoAtuadores from './components/SessaoAtuadores.vue';
</script>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  align-items: center;
  justify-content: center;
}

header {
  text-align: center;
  margin-bottom: 2rem;
}

header h1 {
  font-size: 2rem;
  color: #2c3e50;
  font-weight: 600;
}

main {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

h2 {
    justify-content: center;
    align-items: center;
    text-align: center;
}
</style>
