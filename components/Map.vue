<script setup>
  import "leaflet/dist/leaflet.css";
  import { LMap, LTileLayer } from "@vue-leaflet/vue-leaflet";

  const props = defineProps({
    latLng: Array,
    zoom: Number,
  })

</script>

<template>
  <div style="height: 100%; width: 100%; min-height: 50px;">
    <l-map ref="map" :zoom="zoom" :center="latLng">
      <l-tile-layer
        url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
        layer-type="base"
        name="OpenStreetMap"
      ></l-tile-layer>
      <slot></slot>
    </l-map>
  </div>
</template>
