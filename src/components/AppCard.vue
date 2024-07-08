<script>
export default{
    name:"AppCard",
    props: {
        details: Object
    }
}
</script>

<template>
    <section>
        <div class="card">
            <img :src="details.thumb" alt="">
            <h3>{{ details.series }}</h3>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../assets/styles/variables' as*;

.card {
        width: 150px;
        height: 150px;
        padding-bottom: 20px;
        margin-top: 2rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        text-align: center;
        font-size: 18px;
        color: #333333;

        h3{
            font-size: 10px;
            color: #fff;
            text-align: left;
            margin-top:10px;
        }
    }

    .card img{
      
        width: 100%;
        height: 100%;
        background-repeat: no-repeat;
        background-size: cover;
        display: block;
        cursor: pointer;
     
    }

    .card img:hover {
        box-shadow: 0 4px 8px rgba(1, 81, 172, 0.8);
    }

</style>