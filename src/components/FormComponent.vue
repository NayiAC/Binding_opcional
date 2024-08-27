<script>
export default {
  name: 'FormCompetencias',
  data() {
    return {
      title: '',
      emoji: '',
      apreciacion: '',
      competencias: [],
      opinion: ''
    }
  }
}
</script>
<template>
  <div class="col-4 bg-dark rounded-3 text-white" data-bs-theme="dark">
    <form class="">
      <div class="mb-3">
        <label for="titulo" class="col-sm-2 col-form-label">Titulo</label>
        <div class="col-sm-10">
          <input type="text" class="form-control" id="titulo" v-model="title" />
          <hr />
        </div>
      </div>
      <div class="mb-3">
        <label for="emoji" class="col-sm-2 col-form-label">Emoji</label>
        <select v-model="emoji" class="form-select col-2" aria-label="Selector de emoji">
          <option selected>selecciona un emoji</option>
          <option value="😎">😎</option>
          <option value="🥹">🥹</option>
          <option value="🔥">🔥</option>
          <option value="👩🏽‍💻">👩🏽‍💻</option>
          <option value="🤓">🤓</option>
        </select>
      </div>
      <div class="mb-3">
        <fieldset class="row mb-3">
          <legend class="col-form-label col-sm-2 pt-0 me-2">Apreciación:</legend>
          <div class="col-sm-10">
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gridRadios"
                id="regular"
                value="regular"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="regular"> Regular </label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gridRadios"
                id="bien"
                value="bien"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="bien"> Bien </label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gridRadios"
                id="muybien"
                value="muy bien"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="muybien"> Muy Bien </label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gridRadios"
                id="increible"
                value="increíble ✨"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="increible"> Increíble </label>
            </div>
          </div>
        </fieldset>
      </div>

      <div class="row mb-3">
        <label for="competencias" class="col-sm-2 col-form-label me-2">Competencias:</label>
        <div class="col-sm-10">
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              v-model="competencias"
              value="Morfología de un Componente"
              id="morfologia"
            />
            <label class="form-check-label" for="morfologia"> Morfología de un Componente </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              v-model="competencias"
              value="One way y Two way data binding"
              id="binding"
            />
            <label class="form-check-label" for="binding"> One way y Two way data binding </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              v-model="competencias"
              value="El patrón del diseño MVVM"
              id="elPattrrron"
            />
            <label class="form-check-label" for="elPattrrron"> El patrón del diseño MVVM </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              v-model="competencias"
              value="Directivas"
              id="directivas"
            />
            <label class="form-check-label" for="directivas"> Directivas </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              v-model="competencias"
              value="Estados"
              id="estados"
            />
            <label class="form-check-label" for="estados"> Estados </label>
          </div>
        </div>
      </div>

      <div class="row mb-3">
        <label for="opinion" class="col-sm-2 col-form-label">Opinión</label>
        <div class="col-sm-10">
          <textarea class="form-control" id="opinion" rows="3" v-model="opinion"></textarea>
        </div>
      </div>
    </form>
  </div>
  <div id="resultado" class="col-8 text-center rounded-3">
    <h1>{{ emoji }}</h1>
    <h2>{{ title }}</h2>
    <h3>Y me parece: {{ apreciacion }}</h3>
    <h3>He aprendido:</h3>
    <p>{{ competencias.join(', ') }}.</p>
    <h3>Mi opinión hasta ahora del framework es:</h3>
    <p>{{ opinion }}</p>
  </div>
</template>
<style scoped></style>
