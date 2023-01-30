<template>
  <button class="fr-tag urgent" aria-pressed="true"><slot /></button>
</template>

<style>
button.urgent {
    background-image: radial-gradient(circle at 100% .25rem, transparent .578125rem, rgb(170, 38, 38) .625rem) !important;
  }
</style>
