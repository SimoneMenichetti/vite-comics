<script>
export default{
    name:'AppMain',
}
</script>

<template>
    <main class="main-content">
        <div class="content">
            <!-- Content goes here -->
            <h3> --> Content goes here <--</h3>
        </div>
    </main>
</template>

<style lang="scss"scoped>
@use '../assets/styles/variables';
@use '../assets/styles/general.scss';


// sezione MAIN
.main-content {
    display: flex;
    justify-content: start;
    align-items: center;
    height: calc(100vh - 300px); 
    background-color: black;
   

    .content {
        text-align: center;
        font-size: 16px;
        margin-left: 10rem;
    }
}

</style>