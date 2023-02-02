<template>
  <div>
    <div class="fr-stepper fr-p-2w">
      <h2 class="fr-stepper__title"> <span class="fr-stepper__state">Étape 1 sur 3</span>
        <ul>
          <li>À faire</li>
          <li>En cours</li>
          <li>Terminé</li>
        </ul>
      </h2>
      <div class="fr-stepper__steps" data-fr-current-step="1" data-fr-steps="3"></div>
    </div>
  </div>
</template>

<style scoped>
div.fr-stepper {
  background-color: var(--background-alt-blue-france);
}

ul {
  display: flex;
  justify-content: space-around;
}

li {
  list-style: none;
}
</style>