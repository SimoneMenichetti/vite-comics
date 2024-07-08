<script>
import AppCard from './AppCard.vue';
export default{
    name:'AppMain',
    components: {
        AppCard,
    },
    data(){
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
        <div class="buttoncurrent">
            <button class="currentseries-button"><b>CURRENT SERIES</b></button>
        </div>
        <div class="container">
            <AppCard v-for="(card,i) in cards" :key="i"
            :details="card"/>
        </div>
        <div class="box buttonload">
            <button class="loadmore-button">LOAD MORE</button>
        </div>
            <!-- <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="Action comics">
            <p>ACTION COMICS</p>
        </div>
        <div class="card">
            <img src="https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg" alt="American Vampire">
            <p>AMERICAN VAMPIRE 1976</p>
        </div>
        <div class="card">
            <img src="https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg" alt="acquaman">
            <p>AQUAMAN</p>
        </div>
        <div class="card">
            <img src="https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg" alt="Batgirl">
            <p>BATGIRL</p>
        </div>
        <div class="card">
            <img src="https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg" alt="Batman">
            <P>BATMAN</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg" alt="batmanbeyond">
            <P>BATMAN BEYOND</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg" alt="SupermanVol1">
            <P>BATMAN/SUPERMAN</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg" alt="Batman Superman Vol2">
            <P>BATMAN/SUPERMAN ANNUAL</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg" alt="Batman The joker war vol1">
            <P>BATMAN: THE JOKER WAR ZONE</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg" alt="batman three">
            <P>BATMAN: THREE JOKERS</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg" alt="Harley Quinn">
            <P>BATMAN: WHITE KNIGHT PRESENTS: HARLEY QUINN</P>
        </div>
        <div class="card">
            <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="CatWoman vol 2">
            <P>CATWOMAN</P>
        </div>
    </div> -->
    </main>
</template>

<style lang="scss"scoped>
@use '../assets/styles/variables';
@use '../assets/styles/general.scss';


// sezione MAIN
main{
    background-color: #1C1C1C;
    .container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        height: 450px;
        gap: 20px;
        padding: 20px;
    }

     // generali bottone

     .box {
        text-align: center;

     }
     .loadmore-button, .currentseries-button {
        background-color:  #0282F9;
        color: white;
        padding: 10px 50px;
        margin-bottom: 2rem;
        border: solid 1px #0282F9;
        font-size: 10px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .loadmore-button:hover {
        background-color: #0c5a99;
    }
    .buttoncurrent .currentseries-button{
        position: absolute;
        margin-top: -20px;
        margin-left: 130px;
        padding: 10px 20px;
        font-size: 13px;
        font-weight: bolder;
    }

}

</style>