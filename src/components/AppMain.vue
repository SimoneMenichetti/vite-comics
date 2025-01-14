<script>
// Importazione del componente AppCard per rappresentare le singole card

import AppCard from './common/AppCard.vue';


export default{
    name:'AppMain', // Nome del componente principale
    components: {
        AppCard,   // Registrazione del componente figlio AppCard
    },
    data(){

        // Array di oggetti che rappresentano le card con i dettagli dei fumetti
        return{
            cards:[
            {
                "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book",
            },
            {
                "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book",
            },
            {
                "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel",
            },
            {
                "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book",
            },
            {
                "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel",
            },
            ]
        }
    }
}
</script>

<template>
    <main>
    <!-- Bottone per indicare la serie attuale -->
        <div class="buttoncurrent">
            <button class="currentseries-button"><b>CURRENT SERIES</b></button>
        </div>

        <!-- Contenitore delle card -->
        <div class="container">
         <!-- Creazione dinamica delle card utilizzando il componente AppCard -->
            <AppCard v-for="(card,i) in cards" :key="i"
            :details="card"/>
        </div>
        <div class="box buttonload">
          <!-- Bottone per caricare più contenuti -->
            <button class="loadmore-button">LOAD MORE</button>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/styles/variables';
@use '../assets/styles/general.scss';

main {
    background-color: #1C1C1C;

    .container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;
        padding: 20px;
    }

    .card {
        width: 150px;
        height: 150px;
        padding-bottom: 20px;
        margin-top: 2rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        text-align: center;
        font-size: 18px;
        color: #333333;
    }

    .loadmore-button,
    .currentseries-button {
        background-color: #0282F9;
        color: white;
        padding: 10px 50px;
        margin-bottom: 2rem;
        border: solid 4px #0282F9;
        font-size: 10px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    button:hover {
        background-color: #0c5a99;
    }

    .buttoncurrent .currentseries-button {
        position: absolute;
        margin-top: -20px;
        margin-left: 130px;
        padding: 10px 20px;
        font-size: 13px;
        font-weight: bolder;
    }

    /* container button */
    .box {
        display: flex;
        justify-content: center;
        width: 100%;
        margin-top: 1.5rem;
    }

    /* Responsive media per dispositivi tablet */
    @media (max-width: 768px) {
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            padding: 10px;
        }

        .loadmore-button,
        .currentseries-button {
            width: 35%;
            font-size: 14px;
            padding: 15px;
        }

        .buttoncurrent .currentseries-button {
            margin-left: 10px;
        }
    }

    /* responsive media per dispositivi piccoli smartphone (e.g., 400px) */
    @media (max-width: 400px) {
        .container {
            grid-template-columns: 1fr;  
        }

        .buttoncurrent .currentseries-button {
            margin-left: 10px;  
        }
    }
}
</style>