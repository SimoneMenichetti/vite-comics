<script>
export default{
    name:'AppFeatures',
}
</script>

<template>
      <section class="features">
        <div class="feature">
            <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">
            <p>DIGITAL COMICS</p>
        </div>
        <div class="feature">
            <img src="../assets/img/buy-comics-merchandise.png" alt="DC Merchandise">
            <p>DC MERCHANDISE</p>
        </div>
        <div class="feature">
            <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscription">
            <p>SUBSCRIPTION</p>
        </div>
        <div class="feature">
            <img src="../assets/img/buy-comics-shop-locator.png" alt="Comic Shop Locator">
            <p>COMIC SHOP LOCATOR</p>
        </div>
        <div class="feature">
            <img src="../assets/img/buy-dc-power-visa.svg" alt="DC Power Visa">
            <p>DC POWER VISA</p>
        </div>
    </section>
</template>

<style lang="scss"scoped>
@use'../assets/styles/variables';


.features {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color:#0282F9;
    padding: 30px 140px;


    .feature {
        display: flex;
        align-items: center;
        color: #fff;
        font-size: 14px;
        
    }

    .feature p{
        align-items: center;
    }

    .feature img {
    width: 30px;
    height: 30px;
    margin-right: 1rem;
    
}

}

</style>