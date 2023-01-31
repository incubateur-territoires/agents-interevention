<template>
    <div class="fr-card fr-enlarge-link fr-card--horizontal intervention">
        <div class="fr-card__body">
            <div class="fr-card__content">
                <Tag>Urgent</Tag>
                <p class="fr-card__detail fr-icon-warning-fill">Posté hier à 18h35</p>

                <h3 class="fr-card__title"> <a href="/interventions/1234">
                        15 rue des Dames<br>
                        13002 Marseille
                    </a>
                </h3>
            </div>
        </div>
        <div class="fr-card__header">
            <div class="fr-card__img">
                <img class="fr-responsive-img"
                    src="https://i.pinimg.com/originals/fe/64/99/fe649940d2ea4daa02c5f942fbb88517.jpg"
                    alt="[À MODIFIER - vide ou texte alternatif de l’image]" />
                <!-- L’alternative de l’image (attribut alt) doit toujours être présente, sa valeur peut-être vide (image n’apportant pas de sens supplémentaire au contexte) ou non (porteuse de texte ou apportant du sens) selon votre contexte -->
            </div>
        </div>
    </div>
</template>

<style scoped>
div.intervention {
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
}

div.intervention img {
    max-width: 150px;
    min-height: 150px;
}
</style>