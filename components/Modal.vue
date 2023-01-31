<script setup>
  const props = defineProps({
    open: Boolean
  })
</script>

<template>
  <dialog
    aria-labelledby="fr-modal-title-modal-1"
    role="dialog"
    id="fr-modal-1"
    :class="{ 'fr-modal': true, 'fr-modal--opened': open }"
  >
    <div class="fr-container fr-container--fluid fr-container-md">
      <div class="fr-grid-row fr-grid-row--center">
        <div class="fr-col-12 fr-col-md-8 fr-col-lg-6">
          <div class="fr-modal__body">
            <div class="fr-modal__header">
              <button
                class="fr-link--close fr-link"
                title="Fermer la fenêtre modale"
                aria-controls="fr-modal-1"
                @click="open = false"
              >
                Fermer
              </button>
            </div>
            <div class="fr-modal__content">
              <slot></slot>
            </div>
          </div>
        </div>
      </div>
    </div>
  </dialog>
</template>
