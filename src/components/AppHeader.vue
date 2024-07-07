<script>
export default{
    name:'AppHeader',
    data() {
        return {
            activeLink: '',
            logo: {
            href: "/",
            src: "/public/img/dc-logo.png" ,
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
    }
  }
};

</script>

<template>
    <header>
        <nav class="navbar">
            <div class="logo">
                <a :href="logo.href" class="brand">
                    <img :src="logo.src" :alt="logo.alt">
                </a>
            </div>
            <ul class="nav-links">
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
                <!-- <li>
                    <a href="#">characters</a>
                </li>
                <li>
                    <a href="#">comics</a>
                </li>
                <li>
                    <a href="#">movies</a>
                </li>
                <li>
                    <a href="#">tv</a>
                </li>
                <li>
                    <a href="#">games</a>
                </li>
                <li>
                    <a href="#">collectibles</a>
                </li>
                <li>
                    <a href="#">videos</a>
                </li>
                <li>
                    <a href="#">fans</a>
                </li>
                <li>
                    <a href="#">news</a>
                </li>
                <li>
                    <a href="#">shop</a>
                </li>
            </ul> -->
        </nav>
    </header>
</template>

<style lang="scss"scoped>

@use '../assets/styles/variables' as*;
@use '../assets/styles/mixins' as*;

header{

    .navbar {
        @include center('between');
        padding:1rem;
        
        }
    .logo img {
        height: 50px;
        margin-left: 9rem; 
    }

  
    .nav-links {
        @include center();
        list-style: none;
        margin-right: 8rem;
    }

    .nav-links a {
        text-decoration: none;
        color: black;
        font-weight: bold;
        position: relative;
        padding-bottom: 5px;
    }

    li a{
        padding: 1rem;
        text-decoration: none;
        font-size: 10px;
        font-weight: bold;
        
    }

    .nav-links a:hover,
    .nav-links a.active {
        color:#0282F9;
    }

    .nav-links a:hover::after,
    .nav-links a.active::after {
    content: "";
        position: absolute;
        width: 60%;
        height: 2px;
        background-color: #0282F9;
        bottom: -96%;
        left: 20%;
    }
}

</style>