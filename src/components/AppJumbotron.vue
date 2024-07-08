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
<style lang="scss"scoped>
@use '../assets/styles/variables';
.jumboHeroes {
    position: relative;
    background-image: url('/public/img/jumbotron.jpg'); 
    height: 300px; 
    background-size: cover;
}
</style>