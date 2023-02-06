<template>

  <SubHeader>Intervention 1234</SubHeader>
  <Stepper :current="1" :last="3" :labels="['À faire', 'En cours', 'Terminé']" />
  <InterventionDetails />

  <button class="fr-btn fr-grid-row--center"> <a href="/interventions/1234-en-cours">
      Commencer l'intervention
    </a>
  </button>
</template>

<style scoped>
button {
  width: 100%;
  position: sticky;
  bottom: 0;
}
</style>
