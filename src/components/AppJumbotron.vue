<script>
export default{
    name:'AppJumbotron',
    data() {
        return {
            // jumboHeroes:{
            //     href:"/",
            //     src:"/public/img/jumbotron.jpg",
            //     alt:"jumbo png"
            // },
        }
    }
};
</script>

<template>
    <div class="jumboHeroes">
        <!-- <a :href="jumboHeroes.href">
            <img :src="jumboHeroes.src" :alt="jumboHeroes.alt">
        </a> -->
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/styles/variables';
.jumboHeroes {
    background-image: url('/public/img/jumbotron.jpg'); /* Assicurati che l'immagine sia nella stessa directory del file CSS */
    background-size: cover;
    height: 300px; /* Regola l'altezza secondo le tue necessità */
}
</style>