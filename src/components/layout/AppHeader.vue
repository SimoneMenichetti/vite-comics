<script>
  // Questo componente rappresenta l'header dell'applicazione con un menu di navigazione principale.
  // Include una gestione per il menu a discesa (hamburger menu) per dispositivi mobili.
  import menuLinks from "../../data/menuLinks.json";
  export default {
    name: "AppHeader",
    data() {
      return {
        activeLink: "",
        menuVisible: false,
        logo: {
          href: "/",
          src: "/public/img/dc-logo.png",
          alt: "logo png",
        },
        navLinksData: menuLinks.navLinks, // Importa i dati da menuLinks.json
      };
    },
    methods: {
      setActiveLink(linkText) {
        this.activeLink = linkText;
      },
      toggleMenu() {
        this.menuVisible = !this.menuVisible;
      },
    },
  };
</script>

<template>
  <header>
    <nav class="navbar" role="navigation" aria-label="Main Navigation">
      <div class="logo">
        <a :href="logo.href" class="brand">
          <img :src="logo.src" :alt="logo.alt" />
        </a>
      </div>
      <div class="hamburger" @click="toggleMenu" aria-label="Toggle menu" role="button" tabindex="0">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
      <ul class="nav-links" :class="{ 'menu-visible': menuVisible }" aria-hidden="!menuVisible">
        <li v-for="link in navLinksData" :key="link.text">
          <a
            :href="link.href"
            :class="{ active: link.text === activeLink }"
            @click="setActiveLink(link.text)"
          >
            {{ link.text }}
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>


<style lang="scss" scoped>
@use "../../assets/styles/variables" as *;
@use "../../assets/styles/mixins" as *;

// regole generali header con uso dei mixins
header {
  .navbar {
    @include center("around");
    padding: 1rem;
    position: relative;
  }

  // regole logo
  .logo img {
    height: 60px;
    margin-left: 1rem;
  }

  // regole link navbar
  .nav-links {
    @include center();
    list-style: none;
    margin-right: 8rem;
    gap: 1rem;
  }

  .nav-links a {
    font-weight: bold;
    position: relative;
    padding-bottom: 5px;
  }

  li a {
    padding: 1rem;
    font-size: 14px;
  }

  .nav-links a:hover,
  .nav-links a.active {
    color: #0282f9;
  }

  .nav-links a:hover::after,
  .nav-links a.active::after {
    content: "";
    position: absolute;
    width: 60%;
    height: 4px;
    background-color: #0282f9;
    bottom: -96%;
    left: 20%;
  }

  /* Icona hamburger */
  .hamburger {
    display: none;
    cursor: pointer;
    flex-direction: column;
    gap: 5px;
  }

  .bar {
    width: 30px;
    height: 4px;
    background-color: black;
    border-radius: 5px;
  }

  /* Menu visibile su mobile */
  .nav-links.menu-visible {
    display: block;
    position: absolute;
    top: 70px;
    left: 0;
    right: 0;
    background-color: white;
    padding: 1rem;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    z-index: 10;
  }

  .nav-links.menu-visible li {
    display: block;
    text-align: center;
    padding: 10px 0;
  }

  .nav-links.menu-visible a {
    font-size: 16px;
  }

  /* Responsive modalità desktop */
  @media (max-width: 1024px) { /* Include tablet screen sizes */
    .navbar {
      align-items: center;
    }

    .logo img {
      margin-left: 20px;
    }

     /* Nascondi il menu di default su mobile e tablet */
    .nav-links {
      display: none;
      flex-direction: column;
      margin-right: 0;
      gap: 0;
    }

    /* Mostra l'icona hamburger per mobile e tablet */
    .hamburger {
      display: flex; 
    }
  }
}
</style>
