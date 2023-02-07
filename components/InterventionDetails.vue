<script setup>
import { LMarker, LPopup, LTooltip } from "@vue-leaflet/vue-leaflet";
const images = [
    {
        url: "https://images.unsplash.com/photo-1536849460588-696219a9e98d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1131&q=80",
        tag: "Avant"
    },
    {
        url: "https://images.unsplash.com/photo-1516962080544-eac695c93791?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80",
        tag: "Après"
    }
]
</script>
<template>
    <article class="fr-p-2w">
        <p class="fr-p-2w"> Kevin DUPOND, Stéphane Durand</p>
        <Tag>Urgent</Tag>
        <p class="fr-icon-map-pin-2-line fr-pt-2w"> 16, route de Béthune, 62300 Lens</p>
        <p class="fr-icon-calendar-2-line fr-pt-1w"> Publiée le 23/11/2023 par Jean-Baptiste M.</p>
        <p class="fr-icon-space fr-pt-1w"> Taille : Petit</p>
        <p class="fr-icon-edit-box-line fr-pt-1w"> Support : Mur, Porte</p>
        <slot name="réalisée" />
        <slot name="technique" />
        <p class="fr-mt-3w fr-mb-3w"> Le tag est situé sur la porte de garage et sur le mur situé juste à sa gauche. Il
            y a 4m2 de tags à nettoyer environ.</p>
        <slot />
        <ul class="fr-grid-row fr-grid-row--center images-intervention">
            <li v-for="image in images">
                <p class="fr-tag tags-images" v-if="images.length > 1">{{ image.tag }}</p>
                <img class="fr-responsive-img fr-mb-2w" :src="image.url" alt="image avant intervention" />
            </li>
        </ul>
        <Map :lat-lng="[50.433082, 2.821937]" :zoom=(14) style="height:500px">
            <LMarker :lat-lng="[50.433082, 2.821937]">
                <LTooltip></LTooltip>
                <LPopup>
                    Intervention 1234, Tag
                </LPopup>
            </LMarker>
        </Map>
    </article>
    <hr>
    <InterventionComments />
</template>

<style scoped>
ul.images-intervention {
    flex-wrap: nowrap;
}
li {
    list-style: none;
    position: relative;
}
p.tags-images {
    position: absolute;
    top: 8px;
    left: 8px;
}
</style>
