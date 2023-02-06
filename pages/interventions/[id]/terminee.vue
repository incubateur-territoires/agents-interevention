<template>
  <SubHeader>Intervention 1234</SubHeader>
  <Stepper :current="3" :last="3" :labels="['À faire', 'En cours', 'Terminé']">
  </Stepper>
  <InterventionDetails>
    <section>
      <p slot="réalisée" class="fr-icon-checkbox-circle-line">
        Réalisée le 23/11/2023 par Moussa J.
      </p>
      <p slot="technique" class="fr-icon-brush-3-line fr-pt-1w fr-mb-3w">
        Technique d’effaçage : Hydrogrommage
      </p>
    </section>
  </InterventionDetails>
  <button class="fr-btn fr-grid-row--center">
    <a href="/">
      Revenir à l’accueil
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
