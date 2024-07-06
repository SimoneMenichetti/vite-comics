<script>
export default{
    name:'AppHeader',
    data(){
        return
    }
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

    li a{
        padding: 1rem;
        text-decoration: none;
        font-size: 14px;
        font-weight: bold;
        
    }
}

</style>