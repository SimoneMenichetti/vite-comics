<script>
export default {
  name: "AppHeader",
  data() {
    return {
      activeLink: "",
      menuVisible: false, // Stato per gestire la visibilità del menu a discesa
      logo: {
        href: "/",
        src: "/public/img/dc-logo.png",
        alt: "logo png"
      },
      navLinksData: [
        { href: "#", text: "CHARACTERS" },
        { href: "#", text: "COMICS" },
        { href: "#", text: "MOVIES" },
        { href: "#", text: "TV" },
        { href: "#", text: "GAMES" },
        { href: "#", text: "COLLECTIBLES" },
        { href: "#", text: "VIDEOS" },
        { href: "#", text: "FANS" },
        { href: "#", text: "NEWS" },
        { href: "#", text: "SHOP" }
      ]
    };
  },

  methods: {
    setActiveLink(linkText) {
      this.activeLink = linkText;
    },
    toggleMenu() {
      this.menuVisible = !this.menuVisible; // Alterna la visibilità del menu
    }
  }
};
</script>

<template>
  <header>
    <nav class="navbar">
      <div class="logo">
        <a :href="logo.href" class="brand">
          <img :src="logo.src" :alt="logo.alt" />
        </a>
      </div>
      <!-- Icona hamburger per dispositivi mobili -->
      <div class="hamburger" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
      <!-- Menu a discesa che si attiva al click sull'icona hamburger -->
      <ul class="nav-links" :class="{ 'menu-visible': menuVisible }">
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
@use "../assets/styles/variables" as *;
@use "../assets/styles/mixins" as *;

header {
  .navbar {
    @include center("around");
    padding: 1rem;
    position: relative;
  }

  .logo img {
    height: 60px;
    margin-left: 1rem;
  }

  .nav-links {
    @include center();
    list-style: none;
    margin-right: 8rem;
    display: flex;
    gap: 1rem;
  }

  .nav-links a {
    text-decoration: none;
    color: black;
    font-weight: bold;
    position: relative;
    padding-bottom: 5px;
  }

  li a {
    padding: 1rem;
    text-decoration: none;
    font-size: 14px;
    font-weight: bold;
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
    height: 2px;
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

  /* Responsive adjustments */
  @media (max-width: 1024px) { /* Include tablet screen sizes */
    .navbar {
      align-items: center;
    }

    .logo img {
      margin-left: 20px;
    }

    .nav-links {
      display: none; /* Nascondi il menu di default su mobile e tablet */
      flex-direction: column;
      margin-right: 0;
      gap: 0;
    }

    .hamburger {
      display: flex; /* Mostra l'icona hamburger per mobile e tablet */
    }
  }
}
</style>
