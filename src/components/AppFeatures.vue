<script>
export default{
    name:'AppFeatures',
    data() {
        return {
        featuresData: [
            {
            imgSrc: "/public/img/buy-comics-digital-comics.png",
            imgAlt: "Digital Comics",
            text: "DIGITAL COMICS"
            },
            {
            imgSrc: "/public/img/buy-comics-merchandise.png",
            imgAlt: "DC Merchandise",
            text: "DC MERCHANDISE"
            },
            {
            imgSrc: "/public/img/buy-comics-shop-locator.png",
            imgAlt: "Subscription",
            text: "SUBSCRIPTION"
            },
            {
            imgSrc: "/public/img/buy-comics-shop-locator.png",
            imgAlt: "Comic Shop Locator",
            text: "COMIC SHOP LOCATOR"
            },
            {
            imgSrc: "/public/img/buy-dc-power-visa.svg",
            imgAlt: "DC Power Visa",
            text: "DC POWER VISA"
            }
        ]
        };
    }
};

</script>

<template>
      <section class="features">
        <!-- inizializiamo v for per iterare nel data e dinamicizz img e p -->
        <div v-for="feature in featuresData" :key="feature.text" class="feature">
            <img :src="feature.imgSrc" :alt="feature.imgAlt">
            <p>{{ feature.text }}</p>
        </div>
        <!-- <div class="feature">
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
        </div> -->
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
    cursor: pointer;


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