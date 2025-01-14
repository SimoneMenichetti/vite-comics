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

.features {
    display: flex;
    justify-content: center;
    text-align: center;
    gap: 5rem;
    align-items: center;
    background-color: #0282F9;
    padding: 30px 10px;
    cursor: pointer;
    

    .feature {
        display: flex;
        flex-direction: column;  
        align-items: center; 
        text-align: center;
        color: #fff;
        font-size: 14px;
        margin: 10px;
    }

    .feature img {
        width: 25px;
        height: 25px;
        margin-bottom: 0.5rem;  // Separare l'immagine dal testo
    }

    .feature p {
        margin: 0;
        font-size: 12px;  // Impostato un font più piccolo se necessario
    }
}

// responsive regole generali 

/* Tablet (max-width 768px) */
@media (max-width: 768px) {
    .features {
        padding: 20px 10px;
        justify-content: center;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 1rem;
       
    }
    .feature {
        flex-direction: row; 
        align-items: center;  
    }
}

/* per smartphone (e.g., 400px) */
@media (max-width: 400px) {
    .features {
        padding: 20px 10px;
        justify-content: center;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 1rem;
       
    }

    .feature img {
        width: 20px;
        height: 20px;
    }

    .feature p {
        font-size: 0.8rem;  
    }
}
</style>