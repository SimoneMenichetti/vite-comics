<script>
export default {
    name: 'AppFeatures',
    data() {
        return {
            featuresData: [
                {
                    imgSrc: "/img/buy-comics-digital-comics.png", // Corretto il percorso
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
    <section class="features">
        <div v-for="feature in featuresData" :key="feature.text" class="feature">
            <img :src="feature.imgSrc" :alt="feature.imgAlt">
            <p>{{ feature.text }}</p>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/styles/variables';

// Stili per la sezione delle features
.features {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #0282F9;
    padding: 30px 140px;
    cursor: pointer;
    flex-wrap: wrap;

    .feature {
        display: flex;
        align-items: center; 
        justify-content: center; 
        color: #fff;
        font-size: 14px;
        margin-bottom: 20px;
        width: 150px; 
    }

    .feature p {
        margin-right: 2rem; 
    }

    .feature img {
        width: 30px;
        height: 30px;
        margin-right: 1rem; /* Distanza tra immagine e testo */
    }
}

/* Tablet-sized screens (max-width 768px) */
@media (max-width: 768px) {
    .features {
        padding: 20px 20px;
        justify-content: space-between;
        
       
    }
    
   
}

/* For mobile (e.g., 400px) */
@media (max-width: 400px) {
    .features {
        padding: 20px 10px;
    }

    .feature img {
        width: 25px;
        height: 25px;
    }

    .feature p {
        font-size: 12px;
    }

    .feature {
        justify-content: center;
        width: 100%; 
    }
}
</style>
