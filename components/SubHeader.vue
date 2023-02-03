<script setup>
const props = defineProps({
  closable: Boolean
})
</script>

<template>
  <div>
    <h1 class="fr-p-5v">
      <slot>Page</slot>
    </h1>
    <button v-if="closable">X</button>
  </div>
</template>
