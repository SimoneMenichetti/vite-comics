<script>
export default{
    name:'AppFooter',
}
</script>
<template>
         <footer class="footer">
            <div class="footer-content">
                <div class="footer-top">
                    <div class="footer-column dc-comics-shop">
                        <div class="footer-section">
                            <h3>DC COMICS</h3>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                        </div>
                        <div class="footer-section">
                            <h3>SHOP</h3>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="footer-column">
                        <h3>DC</h3>
                        <ul>
                            <li><a href="#">Terms Of Use</a></li>
                            <li><a href="#">Privacy policy (New)</a></li>
                            <li><a href="#">Ad Choices</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Jobs</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Certificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="#">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                        </ul>
                    </div>
                    <div class="footer-column">
                        <h3>SITES</h3>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>
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
                            <a href="#"><img src="../assets/img/footer-facebook.png" alt="Facebook"></a>
                            <a href="#"><img src="../assets/img/footer-twitter.png" alt="Twitter"></a>
                            <a href="#"><img src="../assets/img/footer-youtube.png" alt="YouTube"></a>
                            <a href="#"><img src="../assets/img/footer-pinterest.png" alt="Pinterest"></a>
                            <a href="#"><img src="../assets/img/footer-periscope.png" alt="Periscope"></a>
                        </div>
                    </div>
                </div>
            
        </footer>
</template>

<style lang="scss"scoped>
    @use '../assets/styles/variables' as*;


// footer
    footer {
        
        background: url('../assets/img/footer-bg.jpg') no-repeat center center/cover;

    .footer-top {
        display: flex;
        justify-content: flex-start;
        padding: 20px 0;
    }

    .footer-content{
        background: url(),url('../assets/img/dc-logo-bg.png') no-repeat 90% center/contain;
      
    }

    .footer-column {
        width: 20%;
     
        margin-right: -80px;
       
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

    .footer-column h3, ul li {
        margin-bottom: 5px;
       margin-left: 160px;
        
    }

    .footer-column ul li a {
        color: #959595;
        text-decoration: none;
        transition: color 0.3s;
    }

    .footer-column ul li a:hover {
        color: #1e90ff;
    }

    .dc-comics-shop {
        display: flex;
        flex-direction: column;
    }

    .dc-comics-shop .footer-section {
        margin-bottom: 20px;
    }

    // FOOTERBOTTOM
    .footer-bottom {
        display: flex;
        justify-content: space-around;
        align-items: center;
        min-height: 70px;
        background-color: #303030;
    }

    // generali bottone
    .signup-button {
        background-color:  #303030;
        color: white;
        padding: 10px 10px;
        margin-right: 13rem;
        border: solid 1px #0282F9;
        font-size: 10px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .signup-button:hover {
        background-color: #0c5a99;
    }


    // sezione icone
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

    
    .followus{
        margin-right: 1rem;
        color: #0282F9;
       
    }
}

</style>