<script setup>
definePageMeta({
  layout: "decorated",
})

const props = defineProps({
  showModal: Boolean
})
</script>

<template>
  <button @click="showModal = true">xxxx</button>
  <Modal :open="showModal">
    <InterventionList />
  </Modal>
</template>