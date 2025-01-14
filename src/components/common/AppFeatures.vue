<script>
export default {
    name: 'AppFeatures',// nome componente principale
    data() {
        return {
            // collezione array delle immagini per le feature del merchandise , pay , position 
            featuresData: [
                {
                    imgSrc: "/img/buy-comics-digital-comics.png",
                    imgAlt: "Digital Comics",
                    text: "DIGITAL COMICS"
                },
                {
                    imgSrc: "/img/buy-comics-merchandise.png",
                    imgAlt: "DC Merchandise",
                    text: "DC MERCHANDISE"
                },
                {
                    imgSrc: "/img/buy-comics-shop-locator.png",
                    imgAlt: "Subscription",
                    text: "SUBSCRIPTION"
                },
                {
                    imgSrc: "/img/buy-comics-shop-locator.png",
                    imgAlt: "Comic Shop Locator",
                    text: "COMIC SHOP LOCATOR"
                },
                {
                    imgSrc: "/img/buy-dc-power-visa.svg",
                    imgAlt: "DC Power Visa",
                    text: "DC POWER VISA"
                }
            ]
        };
    }
};
</script>

<template>
    <!-- sezione features -->
    <section class="features">
    <!-- utilizzo del v-for per dinamicizzare le feauture iterando dalla collezione -->
        <div v-for="feature in featuresData" :key="feature.text" class="feature">
            <img :src="feature.imgSrc" :alt="feature.imgAlt">
            <p>{{ feature.text }}</p>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/styles/variables';

// Stili per la sezione delle features
.features {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: #0282F9;
    padding: 30px 10px;
    cursor: pointer;
    flex-wrap: wrap;

    .feature {
        display: flex;
        align-items: center; 
        justify-content: center; 
        color: #fff;
        font-size: 14px;
        
    }

    .feature p {
        margin-right: 1rem; 
    }

    .feature img {
        width: 25px;
        height: 25px;
        margin-right: 0.5rem; 
    }
}

// responsive regole generali 

/* Tablet (max-width 768px) */
@media (max-width: 768px) {
    .features {
        padding: 30px 10px;
        justify-content: space-around;
        
       
    }

   
}

/* per smartphone (e.g., 400px) */
@media (max-width: 400px) {
    .features {
        padding: 20px 10px;
        justify-content: space-between;
        
    }

    .feature img {
        width: 25px;
        height: 25px;
    }

    .feature p {
        font-size: 0.5rem;
    }

    
}
</style>