<template>
    <h2 class="fr-pr-2w fr-pl-2w">Commentaires</h2>
    <section class="fr-p-2w">
        <!-- <aside>
            Aucun commentaire
        </aside> -->

        <section>
            <ul>
                <li class="fr-responsive-img fr-col-11 fr-mb-1w fr-grid-row--middle comment-agent">
                    <img class="fr-p-1w" src="https://cdn.pixabay.com/photo/2015/07/20/13/01/man-852770_960_720.jpg"
                        alt="">
                    <div>
                        <p class="fr-p-2w fr-mb-1w">
                            Impossible de nettoyer la partie droite, il faut revenir avec plus de détergent.
                        </p>
                        <datetime>01-02-2023</datetime>
                    </div>
                </li>

                <li class="fr-responsive-img fr-col-11 fr-mb-1w fr-grid-row--middle comment-collectivite">
                    <img class="fr-p-1w" src="https://cdn.pixabay.com/photo/2022/06/25/01/46/woman-7282714_960_720.png"
                        alt="">
                    <div class="fr-grid-row--right">
                        <p class="fr-p-2w fr-mb-1w">
                            Ok, on en rachète, on le recevra dans 3 jours.
                        </p>
                        <datetime class="fr-col-4">01-02-2023</datetime>
                    </div>
                </li>
            </ul>
            <h3 class="fr-m-2w fr-grid-row--middle">Aujourd'hui</h3>
            <ul>
                <li class="fr-responsive-img fr-col-11 fr-mb-1w fr-grid-row--middle comment-agent">
                    <img class="fr-p-1w" src="https://cdn.pixabay.com/photo/2015/07/20/13/01/man-852770_960_720.jpg"
                        alt="">
                    <div>
                        <p class="fr-p-2w fr-mb-1w">
                            C’est nettoyé. La mission est terminée.
                        </p>
                        <datetime>01-02-2023</datetime>
                    </div>
                </li>
            </ul>
        </section>
        <form class="fr-p-2w comment">
            <textarea class="fr-col-12 fr-p-1w fr-pr-6w" placeholder="Ecrire un message" />
            <button class="fr-icon-send-plane-fill comment-button" type="submit"></button>
        </form>
    </section>

</template>

<style scoped>
li {
    list-style: none;
    display: flex;
}

img {
    max-width: 75px;
    max-height: 75px;
    border-radius: 100%;
}

li.comment-agent p {
    background-color: var(--background-alt-blue-france);
    border-radius: 16px 16px 16px 0px;
}

li.comment-collectivite {
    flex-direction: row-reverse;
}

li.comment-collectivite div {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}

li.comment-collectivite p {
    box-shadow: 0 0 0 1px var(--border-default-grey);
    border-radius: 16px 16px 0px 16px;
}

textarea {
    box-shadow: 0 0 0 1px var(--border-default-grey);
    border-radius: 10px;
}

button.comment-button {
    color: var(--background-active-blue-france);
    position: absolute;
    right: 24px;
    top: 30px;
}

h3 {
    background-color: var(--border-default-grey);
    border-radius: 10px;
    display: inline-block;
}

h3:after {
    content: "-";
}

h3:before {
    content: "-";
}

form{
    position: relative;
}
</style>