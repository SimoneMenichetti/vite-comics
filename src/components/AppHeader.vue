<script>
export default{
    name:'AppHeader',
}
</script>

<template>
    <header>
        
        <nav class="navbar">
            <div class="logo">
                <a href="/" class="brand">
                    <img src="../assets/img/dc-logo.png" alt="logo png">
                </a>
            </div>
            <ul class="nav-links">
                <li>
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
            </ul>
        </nav>
    </header>
</template>

<style lang="scss"scoped>

@use '../assets/styles/variables' as*;
@use '../assets/styles/mixins' as*;

header{
  

    .navbar {
        @include center('between');
        padding: 5rem;
        
        }
    .logo img {
        height: 60px;
        margin-left: 6rem; 
    }

  
    .nav-links {
        @include center();
        list-style: none;
        padding: 0;
        margin-right: 4rem;
    }

    li a{
        padding: 1rem;
        text-decoration: none;
        
    }
}

</style>