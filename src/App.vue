<script>
export default {
  data() {
    return {
      title: 'Estoy aprendiendo Vue',
      appreciation: 'Increíble',
      emoji: '👨‍💻',
      competencia: [ ],
      opinion: '',
    }
    }
  }

</script>

<template>
  <div id="app">
    <div class="container row">

      <div class="col-6 container p-4 bg-dark text-white rounded">
        <div class="mb-3">
          <label for="title" class="form-label">Título:</label>
          <input type="text" class="form-control" id="title" v-model="title" placeholder="Estoy aprendiendo Vue">
        </div>

        <div class="mb-3">
          <label for="emoji" class="form-label">Emoji:</label>
          <select class="form-select" id="emoji" v-model="emoji">
            <option value="👨‍💻">👨‍💻</option>
            <option value="😎">😎</option>
            <option value="😒">😒</option>
          </select>
        </div>

        <div class="mb-3">
          <label class="form-label">Apreciación:</label><br>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio" v-model="appreciation" name="appreciation" id="regular" value="regular">
            <label class="form-check-label" for="regular">Regular</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio"v-model="appreciation" name="appreciation" id="bien" value="bien">
            <label class="form-check-label" for="bien">Bien</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio"v-model="appreciation" name="appreciation" id="muy-bien" value="muy bien">
            <label class="form-check-label" for="muy-bien">Muy bien</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio"v-model="appreciation" name="appreciation" id="increible" value="increible" checked>
            <label class="form-check-label" for="increible">Increíble</label>
          </div>
        </div>

        <div class="mb-3">
          <label class="form-label">Competencias aprendidas:</label><br>
          <div class="form-check form-check-inline">
            <input class="form-check-input" v-model="competencia" value="Morfología de un componente" type="checkbox" id="competencia1" >
            <label class="form-check-label" for="competencia1">Morfología de un componente</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" v-model="competencia" value="Directivas" type="checkbox" id="competencia2">
            <label class="form-check-label" for="competencia2">Directivas</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" v-model="competencia" value="One-Way y Two-Way data binding" type="checkbox" id="competencia3" >
            <label class="form-check-label" for="competencia3">One-Way y Two-Way data binding</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" v-model="competencia" value="Estado" type="checkbox" id="competencia4">
            <label class="form-check-label" for="competencia4">Estado</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" v-model="competencia" value="El Patrón de diseño" type="checkbox" id="competencia5">
            <label class="form-check-label" for="competencia5">El patrón de diseño MVVM</label>
          </div>
        </div>

        <div class="mb-3">
          <label for="opinion" class="form-label">Opinión:</label>
          <textarea class="form-control" v-model="opinion" id="opinion" placeholder="Escriba su opinión"
            rows="3"></textarea>
        </div>
      </div>

      <div class="col-6">
        <h3>{{ emoji }}</h3>
        <h1> {{ title }}</h1>
        <h5>Y me parece {{ appreciation }}</h5>
        <h5>He aprendido: </h5>
        <p class="bold"> {{ competencia.join(' -/- ') }}</p>
        <h5>Mi opinion:</h5>
        <p>{{ opinion }}</p>
      </div>
    </div>
  </div>
</template>

<style></style>
