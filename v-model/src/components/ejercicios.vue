<!-- Seccion de JS -->
<script>
export default {
  name: "ejercicios",
  data() {
    return {
      seleccionAnimal: null,
    };
  },
};
</script>

<!-- Seccion de HTML -->
<template>
  <div id="ejercicios">
    <!-- ejercicio select Animal y muestra la imagen -->
    <form>
      <label>Selecciona el Animal:</label>
      <select v-model="seleccionAnimal">
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/5/56/Tiger.50.jpg"
        >
          Tigre
        </option>
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/7/73/Lion_waiting_in_Namibia.jpg"
        >
          León
        </option>
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/3/37/Oryctolagus_cuniculus_Tasmania_2.jpg"
        >
          Conejo
        </option>
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/6/6e/Golden_Retriever_Carlos_%2810581910556%29.jpg"
        >
          Perro
        </option>
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/4/4d/Cat_November_2010-1a.jpg"
        >
          Gato
        </option>
        <option
          value="https://upload.wikimedia.org/wikipedia/commons/7/70/Common_seal_%28Phoca_vitulina%29_swimming.jpg"
        >
          Foca
        </option>
      </select>
      <div style="display: block">
        <img :src="seleccionAnimal" height="200" />
      </div>
    </form>
  </div>
</template>

<!-- Seccion de CSS -->
<style scoped></style>
