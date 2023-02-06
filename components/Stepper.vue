<script setup>
const props = defineProps({
  current: Number,
  last: Number,
  labels: Array
})
</script>


<template>
  <div>
    <div class="fr-stepper fr-p-2w">
      <h2 class="fr-stepper__title"> <span class="fr-stepper__state">Étape {{ current }} sur {{ last }}</span>
        <ul>
          <li v-for="label in labels">{{ label }}</li>
        </ul>
      </h2>
      <div class="fr-stepper__steps" :data-fr-current-step="current" :data-fr-steps="last"></div>
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
