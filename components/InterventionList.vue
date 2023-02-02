<template>
    <SubHeader>Liste des interventions</SubHeader>
    <ul class="tags">
        <ul class="fr-tags-group">
            <li>
                <Tag>Urgent</Tag>
            </li>
            <li>
                <Tag>Normal</Tag>
            </li>
        </ul>

        <ul class="fr-tags-group tags-types-interventions">
            <li>
                <Tag>Espace Vert</Tag>
            </li>
            <li>
                <Tag>Voirie</Tag>
            </li>
            <li>
                <Tag>Propreté</Tag>
            </li>
            <li>
                <Tag>Autres</Tag>
            </li>
        </ul>
    </ul>

    <h3>10 interventions</h3>

    <ul>
        <li>
            <Intervention />
        </li>
        <li>
            <Intervention />
        </li>
        <li>
            <Intervention />
        </li>
        <li>
            <Intervention />
        </li>
    </ul>
</template>


<style scoped>
.tags {
    display: flex;
}

.tags-types-interventions {
    border-left: 2px solid #000;
}

li{
    list-style: none;
}
</style>