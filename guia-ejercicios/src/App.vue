<script>
export default {
  name: "App",
  data() {
    return {
      usuario: {
        nombre: "",
        nacionalidad: "",
        genero: "",
        direccion: "",
        estadoCivil: "",
        continentes: [],
      },
    };
  },
};
</script>

<template>
  <div id="app">
    <h1 class="ms-5">Guia de Ejercicios</h1>
    <form class="planillaUsuario">
      <div class="mb-3">
        <label class="form-label fw-bold">Nombre</label>
        <input class="form-control" v-model="usuario.nombre" />
      </div>

      <div class="mb-3">
        <label class="form-label fw-bold"> Nacionalidad </label>
        <select class="form-select" v-model="usuario.nacionalidad">
          <option value="Chile">Chile</option>
          <option value="Extranjero">Extranjero</option>
        </select>
      </div>
      <!-- Genero -->
      <div class="mb-3">
        <label class="form-label fw-bold">Genero</label>
        <div class="d-flex gap-3">
          <div class="form-check">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="m"
              value="masculino"
              v-model="usuario.genero"
            />
            <label class="form-check-label fw-normal" for="m">
              masculino
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="f"
              value="femenino"
              v-model="usuario.genero"
            />
            <label class="form-check-label fw-normal" for="f"> femenino </label>
          </div>
        </div>
      </div>
      <!-- dirección -->
      <div class="mb-3">
        <label class="form-label fw-bold">Dirección</label>
        <input class="form-control" v-model="usuario.direccion" />
      </div>
      <!-- estado civil -->
      <div class="mb-3">
        <label class="form-label fw-bold">Estado civil</label>
        <div class="d-flex gap-3">
          <div class="form-check">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="soltero"
              value="Soltero"
              v-model="usuario.estadoCivil"
            />
            <label class="form-check-label fw-normal" for="soltero">
              Soltero
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="casado"
              value="Casado"
              v-model="usuario.estadoCivil"
            />
            <label class="form-check-label fw-normal" for="casado">
              Casado
            </label>
          </div>
        </div>
      </div>
      <!-- continentes -->
      <div class="mb-3">
        <label class="form-label fw-bold">Continentes que he visitado</label>
        <div class="d-flex gap-3 flex-wrap">
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="america"
              value="America"
              v-model="usuario.continentes"
            />
            <label class="form-check-label fw-normal" for="america">
              América
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="europa"
              value="Europa"
              v-model="usuario.continentes"
            />
            <label class="form-check-label fw-normal" for="europa">
              Europa
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="asia"
              value="Asia"
              v-model="usuario.continentes"
            />
            <label class="form-check-label fw-normal" for="asia"> Asia </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="africa"
              value="Africa"
              v-model="usuario.continentes"
            />
            <label class="form-check-label fw-normal" for="africa">
              África
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="oceania"
              value="Oceania"
              v-model="usuario.continentes"
            />
            <label class="form-check-label fw-normal" for="oceania">
              Oceanía
            </label>
          </div>
        </div>
      </div>
    </form>
    <div class="planilla text-center mt-5 w-75">
      <h2 clas>Planilla de Usuario</h2>
      <hr />
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Nombre</th>
            <th>Nacionalidad</th>
            <th>Género</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ usuario.nombre }}</td>
            <td>{{ usuario.nacionalidad }}</td>
            <td>{{ usuario.genero }}</td>
          </tr>
        </tbody>
      </table>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Dirección</th>
            <th>Estado civil</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ usuario.direccion }}</td>
            <td>{{ usuario.estadoCivil }}</td>
          </tr>
        </tbody>
      </table>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>Continentes que ha visitado</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>{{ usuario.continentes }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style>
.planillaUsuario {
  width: 30%;
  margin-left: 30px;
  border: 1px solid gray;
  border-radius: 10px;
  padding: 1rem;
}

.table {
  width: 70%;
  margin-left: 30px;
}
</style>
