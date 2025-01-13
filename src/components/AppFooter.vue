
<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            footerSections: [
                {
                    title: 'DC COMICS',
                    items: [
                        { label: 'Characters', url: '#' },
                        { label: 'Comics', url: '#' },
                        { label: 'Movies', url: '#' },
                        { label: 'TV', url: '#' },
                        { label: 'Games', url: '#' },
                        { label: 'Videos', url: '#' },
                        { label: 'News', url: '#' }
                    ]
                },
                {
                    title: 'SHOP',
                    items: [
                        { label: 'Shop DC', url: '#' },
                        { label: 'Shop DC Collectibles', url: '#' }
                    ]
                },
                {
                    title: 'DC',
                    items: [
                        { label: 'Terms Of Use', url: '#' },
                        { label: 'Privacy policy (New)', url: '#' },
                        { label: 'Ad Choices', url: '#' },
                        { label: 'Advertising', url: '#' },
                        { label: 'Jobs', url: '#' },
                        { label: 'Subscriptions', url: '#' },
                        { label: 'Talent Workshops', url: '#' },
                        { label: 'CPSC Certificates', url: '#' },
                        { label: 'Ratings', url: '#' },
                        { label: 'Shop Help', url: '#' },
                        { label: 'Contact Us', url: '#' }
                    ]
                },
                {
                    title: 'SITES',
                    items: [
                        { label: 'DC', url: '#' },
                        { label: 'MAD Magazine', url: '#' },
                        { label: 'DC Kids', url: '#' },
                        { label: 'DC Universe', url: '#' },
                        { label: 'DC Power Visa', url: '#' }
                    ]
                }
            ],
            socialIcons: [
                { image: '/img/footer-facebook.png', alt: 'Facebook', url: '#' },
                { image: '/img/footer-twitter.png', alt: 'Twitter', url: '#' },
                { image: '/img/footer-youtube.png', alt: 'YouTube', url: '#' },
                { image: '/img/footer-pinterest.png', alt: 'Pinterest', url: '#' },
                { image: '/img/footer-periscope.png', alt: 'Periscope', url: '#' }
            ]
        };
    }
};
</script>

<template>
    <footer class="footer">
        <div class="footer-content">
            <div class="footer-top">
                <div class="footer-column dc-comics-shop">
                    <div class="footer-section">
                        <h3>{{ footerSections[0].title }}</h3>
                        <ul>
                            <li v-for="(item, i) in footerSections[0].items" :key="i"><a :href="item.url">{{ item.label }}</a></li>
                        </ul>
                    </div>
                    <div class="footer-section">
                        <h3>{{ footerSections[1].title }}</h3>
                        <ul>
                            <li v-for="(item, i) in footerSections[1].items" :key="i"><a :href="item.url">{{ item.label }}</a></li>
                        </ul>
                    </div>
                </div>
                <div class="footer-column" v-for="(section, index) in footerSections.slice(2)" :key="index">
                    <h3>{{ section.title }}</h3>
                    <ul>
                        <li v-for="(item, i) in section.items" :key="i"><a :href="item.url">{{ item.label }}</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <div class="footer-middle">
                    <button class="signup-button">SIGN-UP NOW!</button>
                </div>
                <div class="social-icons">
                    <div class="followus">
                        <p>FOLLOW US</p>
                    </div>
                    <a v-for="(icon, i) in socialIcons" :key="i" :href="icon.url"><img :src="icon.image" :alt="icon.alt"></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/styles/variables' as *;

footer {
    background: url('/img/footer-bg.jpg') no-repeat center center/cover;

    .footer-content {
        background: url('/img/dc-logo-bg.png') no-repeat 90% center /contain;
    }

    .footer-section h3{
        margin-top: 5px;
    }

    .footer-top {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        padding: 20px 0;
        
    }

    .footer-column {
        margin-right: 20px;
        margin-bottom: 10px;
        min-width: 180px; 
    }

    .footer-column h3 {
        font-size: 14px;
        margin-bottom: 10px;
    }


    .footer-column ul {
        list-style: none;
        font-size: 10px;
        padding: 0;
        
    }

    .footer-column ul li a {
        color: #959595;
        text-decoration: none;
        transition: color 0.3s;
      
    }

    .footer-column ul li a:hover {
        color: #1e90ff;
    }

    .footer-bottom {
        display: flex;
        justify-content: space-around;
        align-items: center;
        min-height: 70px;
        background-color: #303030;
    }

    .signup-button {
        background-color: #303030;
        color: white;
        padding: 10px 10px;
        border: solid 1px #0282F9;
        font-size: 10px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .signup-button:hover {
        background-color: #0c5a99;
    }

    .social-icons {
        display: flex;
        align-items: center;
    }

    .social-icons a {
        margin: 0 10px;
    }

    .social-icons img {
        width: 24px;
        height: 24px;
    }

    .followus {
        margin-right: 1rem;
        color: #0282F9;
    }

    /* Responsive adjustments */
    @media (max-width: 800px) {
        .footer-top {
            display: flex;
           
            align-items: center;
            flex-wrap: wrap;
            text-align: center; 
        }

        .footer-column {
            margin-bottom: 20px;
            justify-content: space-evenly;
        }


        .footer-bottom {
            flex-direction: column;
            align-items: center;
            padding: 20px 10px;
        }

        .signup-button {
         margin-bottom: 1rem;
    }

    }

    @media (max-width: 400px) {
    .footer-top {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        text-align: center; 
    }

    .footer-column {
        flex: 0 0 100%; 
        margin-bottom: 20px;
    }
}
}


</style>
