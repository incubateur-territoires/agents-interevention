<template>
  <SubHeader>Intervention 1234</SubHeader>
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
  <ul class="fr-btns-group">
    <li>
      <button class="fr-btn fr-btn--secondary">Continuer sans photo</button>
    </li>
    <li>
      <button class="fr-btn">Prendre une photo</button>
    </li>
  </ul>
</template>

<style scoped>
button {
  width: 100%;
  position: sticky;
  bottom: 0;
}
</style>
