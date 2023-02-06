<script setup>
import { LMarker, LPopup, LTooltip } from "@vue-leaflet/vue-leaflet";
</script>
<template>
    <article class="fr-p-2w">
        <p class="fr-p-2w"> Kevin DUPOND, Stéphane Durand</p>
        <Tag>Urgent</Tag>
        <p class="fr-icon-map-pin-2-line fr-pt-2w"> 16, route de Béthune, 62300 Lens</p>
        <p class="fr-icon-calendar-2-line fr-pt-1w"> Publiée le 23/11/2023 par Jean-Baptiste M.</p>
        <p class="fr-icon-space fr-pt-1w"> Taille : Petit</p>
        <p class="fr-icon-edit-box-line fr-pt-1w"> Support : Mur, Porte</p>
        <p class="fr-mt-3w fr-mb-3w"> Le tag est situé sur la porte de garage et sur le mur situé juste à sa gauche. Il
            y a 4m2 de tags à nettoyer environ.</p>
        <slot />
        <img class="fr-responsive-img fr-mb-2w"
            src="https://i.pinimg.com/originals/fe/64/99/fe649940d2ea4daa02c5f942fbb88517.jpg"
            alt="[À MODIFIER - vide ou texte alternatif de l’image]" />
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

