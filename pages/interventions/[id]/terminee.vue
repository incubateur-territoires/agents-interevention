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
  <a href="/" class="fr-btn fr-grid-row--center">
    Revenir à l’accueil
  </a>
</template>

<style scoped>
a {
  width: 100%;
  position: sticky;
  bottom: 0;
}
</style>
