<template>
  <div>
    <div class="fr-skiplinks">
      <nav class="fr-container" role="navigation" aria-label="Accès rapide">
        <ul class="fr-skiplinks__list">
          <li>
            <a class="fr-btn" href="#main-content">Aller au contenu principal</a>
          </li>
          <li><a class="fr-btn" href="#header-navigation">Menu</a></li>
          <li><a class="fr-btn" href="#fr-footer-1">Pied de page</a></li>
        </ul>
      </nav>
    </div>
    <header role="banner" class="fr-header">
      <div class="fr-header__body">
        <div class="fr-container">
          <div class="fr-header__body-row">
            <div class="fr-header__brand fr-enlarge-link">
              <div class="fr-header__brand-top">
                <div class="fr-header__logo">
                  <p class="fr-logo">
                    République
                    <br />Française
                  </p>
                </div>
                <div class="fr-header__navbar">
                  <button id="fr-btn-menu-mobile" class="fr-btn--menu fr-btn" :data-fr-opened="menuOpened"
                    aria-controls="header-navigation" aria-haspopup="menu" title="Menu" aria-label="Menu"
                    @click="showMenu">
                    Menu
                  </button>
                </div>
              </div>
            </div>
            <div class="fr-header__tools">
              <div class="fr-header__tools-links">
                <ul class="fr-links-group">
                  <li>
                    <nuxt-link :to="{ name: 'contact' }" class="fr-link fr-icon-mail-line">Nous contacter</nuxt-link>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div id="header-navigation" class="fr-header__menu fr-modal" :class="{ 'fr-modal--opened': modalOpened }"
        aria-labelledby="fr-btn-menu-mobile">
        <div class="fr-container">
          <button class="fr-link--close fr-link" aria-controls="header-navigation" @click="hideModal">
            Fermer
          </button>
          <div class="fr-header__menu-links"></div>
          <nav id="main-navigation" class="fr-nav" role="navigation" aria-label="Menu principal">
            <ul class="fr-nav__list">
              <li class="fr-nav__item">
                <nuxt-link class="fr-nav__link" to="/">Accueil</nuxt-link>
              </li>
              <li class="fr-nav__item">
                <nuxt-link class="fr-nav__link" :to="{ name: 'contact' }">Contact</nuxt-link>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'FrHeader',

  data: () => ({
    menuOpened: false,
    modalOpened: false,
    offerMenuOpened: false,
  }),

  methods: {
    hideModal() {
      this.modalOpened = false;
      this.menuOpened = false;
    },
    showMenu() {
      this.modalOpened = true;
      this.menuOpened = true;
    },
    toggleDropdown() {
      this.offerMenuOpened = !this.offerMenuOpened;
    },
    closeDropDown() {
      if (this.offerMenuOpened) {
        this.offerMenuOpened = false;
      }
    },
  },
};
</script>

<style scoped>
.anct-special-label {
  position: relative;
  z-index: 500;
}

.anct-special-label::after {
  content: 'Nouveau';
  position: absolute;
  z-index: 1000;
  top: 3px;
  left: 50%;
  height: fit-content;
  line-height: 19px;
  font-size: 11px;
  font-weight: bold;
  color: white;
  background-color: #00ac8c;
  border-radius: 13px;
  padding: 0 0.8rem;
}

.after-special-label {
  position: relative;
  z-index: 0;
}

.fr-nav__item>.fr-nav__link.nuxt-link-active,
.fr-nav__btn.nuxt-link-active {
  position: relative;
}

.fr-nav__item>.fr-nav__link.nuxt-link-active::before,
.fr-nav__btn.nuxt-link-active::before {
  background-color: var(--text-active-blue-france);
  bottom: 0;
  content: '';
  height: 2px;
  left: 0;
  position: absolute;
  top: auto;
  width: 100%;
}

@media screen and (max-width: 991px) {
  .anct-special-label::after {
    top: 32%;
    left: 8%;
  }
}

@media screen and (max-width: 600px) {
  .anct-special-label::after {
    top: 32%;
    left: 18%;
  }
}
</style>
