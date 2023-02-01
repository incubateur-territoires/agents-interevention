<template>
    <h4>Commentaires</h4>
    <section>
        <aside>
            Aucun commentaire
        </aside>

        <section>
            <ul>
                <li class="fr-responsive-img fr-p-1w fr-col-10 comment-agent">
                    <img class="fr-p-1w" src="https://cdn.pixabay.com/photo/2015/07/20/13/01/man-852770_960_720.jpg"
                        alt="">
                    <div>
                        <p class="fr-p-2w">
                            Impossible de nettoyer la partie droite, il faut revenir avec plus de détergent.
                        </p>
                        <datetime>01-02-2023</datetime>
                    </div>
                </li>

                <li class="fr-responsive-img fr-p-1w fr-col-10 comment-collectivite">
                    <img class="fr-p-1w" src="https://cdn.pixabay.com/photo/2022/06/25/01/46/woman-7282714_960_720.png"
                        alt="">
                    <div>
                        <p class="fr-p-2w">
                            Ok, on en rachète, on le recevra dans 3 jours.
                        </p>
                        <datetime>01-02-2023</datetime>
                    </div>
                </li>
            </ul>
        </section>
        <form>
            <textarea id="comment" rows="3" cols="50" placeholder="Ecrire un message" />
            <button class="fr-icon-send-plane-fill" type="submit"></button>
        </form>
    </section>

</template>

<style scoped>
img {
    max-width: 75px;
    max-height: 75px;
    border-radius: 100%;
}

ul,
li,
p {
    padding: 0;
    margin: 0;
}

ul {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

li {
    list-style: none;
    display: flex;
    align-items: center;
}

li.comment-agent p {
    background-color: var(--background-alt-blue-france);
}

li.comment-collectivite {
    flex-direction: row-reverse;
}
li.comment-collectivite p {
    box-shadow: 0 0 0 1px var(--border-default-grey);
}

li.comment-collectivite div {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}

p {
    border-radius: 16px;
}
</style>