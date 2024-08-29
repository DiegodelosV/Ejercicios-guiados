<!-- Seccion de JS -->
<script>
export default {
  name: "App",
  data() {
    return {
      seleccionAnimal: null,
      nombreDelCurso: "",
      numeroDeTelefono: "",
      ciudadSrc:
        "https://upload.wikimedia.org/wikipedia/commons/f/ff/Laguna_Espejo._futaleuf%C3%BA.JPG",
      bannerSRC: "",
      inputDinamico: "",
      letra: "",
      color: "",
      generos: [],
      form: {
        titulo: "",
        comentario: "",
      },
    };
  },
};
</script>

<!-- Seccion de HTML -->
<template>
  <div id="app">
    <!-- Ejercicio select Animal y muestra la imagen -->
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

    <!-- Ejercicio mostrar nombre del curso -->
    <h1>
      Bienvenido al curso de <span>{{ nombreDelCurso }}</span>
    </h1>
    <input v-model="nombreDelCurso" />

    <h2>Teléfono</h2>
    <h2>Para más información contactarse al número {{ numeroDeTelefono }}</h2>
    <input v-model="numeroDeTelefono" />

    <!-- Ejercicio mostrar imagen -->
    <h2>Mi Ciudad Favorita: Futaleufú</h2>
    <img width="500px" :src="ciudadSrc" />

    <!-- Ejercicio URL dinámica -->
    <div class="con">
      <form>
        <label>Banner</label>
        <input v-model="bannerSRC" />
      </form>
      <img :src="bannerSRC" height="200" />
    </div>

    <!-- Ejercicio input dinámico -->
    <h2>Input Dinámico</h2>
    <p>{{ inputDinamico }}</p>
    <input v-model="inputDinamico" />

    <!-- Ejercicio select -->
    <form>
      <label>Animal: </label>
      <select v-model="letra">
        <option value="a">A</option>
        <option value="b">B</option>
        <option value="c">C</option>
        <option value="d">D</option>
        <option value="e">E</option>
        <option value="f">F</option>
      </select>
    </form>

    <!-- Ejercicio radio buttons -->

    <h2>Selector de Colores</h2>
    <h2>Radio</h2>
    <form>
      <label> Seleccion el color de su producto: {{ color }}</label>
      <ul>
        <li>
          <input type="radio" value="red" v-model="color">
          Rojo
        </li>
        <li>
          <input type="radio" value="green" v-model="color">
          Verde
        </li>
        <li>
          <input type="radio" value="blue" v-model="color">
          Azul
        </li>
      </ul>
    </form>
    <div class="color-box" :style="{ backgroundColor: color }"></div>

    <!-- Ejercicio checkboxes -->
    <form class="generos">
      <label>¿Qué géneros musicales prefieres?: </label>
      <ul>
        <li>
          <input type="checkbox" value="Rock" v-model="generos" />
          <label>Rock</label>
        </li>
        <li>
          <input type="checkbox" value="Baladas" v-model="generos" />
          <label>Baladas</label>
        </li>
        <li>
          <input type="checkbox" value="Urbano" v-model="generos" />
          <label>Urbano</label>
        </li>
        <li>
          <input type="checkbox" value="Jazz" v-model="generos" />
          <label>Jazz</label>
        </li>
        <li>
          <input type="checkbox" value="Blues" v-model="generos" />
          <label>Blues</label>
        </li>
        <li>
          <input type="checkbox" value="Pop" v-model="generos" />
          <label>Pop</label>
        </li>
        <li>
          <input type="checkbox" value="Otros" v-model="generos" />
          <label>Otros</label>
        </li>
      </ul>
    </form>

    <p>{{ generos }}</p>

    <!-- Ejercicio formulario -->
    <form class="generos">
      <label>Título</label>
      <input type="text" v-model="form.titulo" />
      <label>Contenido</label>
      <textarea v-model="form.comentario"></textarea>
    </form>

    <p>{{ form }}</p>
  </div>
</template>

<!-- Seccion de CSS -->
<style scoped>
span {
  color: #3fb27f;
}

.generos {
  display: flex;
  flex-direction: column;
  border: #3fb27f 1px solid;
  box-shadow: 5px 5px 5px #3fb27f;
  padding: 10px;
  width: 300px;
  border-radius: 30px;
}

.color-box {
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
</style>
