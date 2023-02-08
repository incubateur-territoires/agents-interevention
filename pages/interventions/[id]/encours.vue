<script setup>
import { ref } from 'vue'
let imageData = ref("")

function previewImage(event) {
  const file = event.target.files[0]

  const reader = new FileReader()
  reader.onload = (e) => {
    imageData.value = e.target.result
  }
  reader.readAsDataURL(file)
}

const props = defineProps({
  showModal: Boolean
})
</script>

<template>
  <SubHeader>Intervention 1234</SubHeader>
  <Stepper :current="2" :last="3" :labels="['À faire', 'En cours', 'Terminé']">
  </Stepper>
  <InterventionDetails>
    <section>
      <h2>Méthode d’effaçage utilisée :</h2>

      <ul class="fr-toggle__list">
        <li>
          <div class="fr-toggle fr-toggle--border-bottom fr-toggle--label-left">
            <input type="checkbox" class="fr-toggle__input" id="group-4-toggle-0">
            <label class="fr-toggle__label" for="group-4-toggle-0">
              Hydrogommage
            </label>
          </div>
        </li>
        <li>
          <div class="fr-toggle fr-toggle--border-bottom fr-toggle--label-left">
            <input type="checkbox" class="fr-toggle__input" id="group-4-toggle-1">
            <label class="fr-toggle__label" for="group-4-toggle-1">
              Lavage</label>
          </div>
        </li>
        <li>
          <div class="fr-toggle fr-toggle--border-bottom fr-toggle--label-left">
            <input type="checkbox" class="fr-toggle__input" id="group-4-toggle-2">
            <label class="fr-toggle__label" for="group-4-toggle-2">
              Peinture</label>
          </div>
        </li>
        <li>
          <div class="fr-toggle fr-toggle--border-bottom fr-toggle--label-left">
            <input type="checkbox" class="fr-toggle__input" id="group-4-toggle-3">
            <label class="fr-toggle__label" for="group-4-toggle-3">
              Autres</label>
          </div>
        </li>
      </ul>
    </section>
  </InterventionDetails>

  <ul class="fr-btns-group" id="photo">
    <li>
      <a class="fr-btn fr-btn--secondary" href="/interventions/1234/confirmation">
        Continuer sans photo
      </a>
    </li>
    <li>
      <input type="file" ref="fileInput" capture="environment" accept="image/*" id="file" @change="previewImage"
        @click="showModal = true">
      <label for="file" class="fr-btn">
        Prendre une photo
      </label>
    </li>
  </ul>
  <Modal :open="showModal">
    <SubHeader>Intervention 1234</SubHeader>
    <div v-if="imageData">
      <img class="fr-responsive-img" :src="imageData">
    </div>
    <button class="fr-btn fr-grid-row--center">
      <a href="/interventions/1234/confirmation">
        Ajouter la photo
      </a>
    </button>
  </Modal>
</template>

<style scoped>
input[type="file"] {
  height: 0;
  width: 0;
  overflow: hidden;
}

ul {
  position: sticky;
  bottom: 0;
  background-color: var(--background-default-grey);
}

button,
label {
  width: 100%;
}
</style>
