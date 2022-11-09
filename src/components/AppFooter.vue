<script>
export default{
    name: "AppFooter",
    data(){
        return{
            dcComicsLinks: [
                {
                    title: "Characters",
                    href: "/characters",
                },
                {
                    title: "Comics",
                    href: "/comics",
                },
                {
                    title: "Movies",
                    href: "/movies",
                },
                {
                    title: "TV",
                    href: "/tv",
                },
                {
                    title: "Games",
                    href: "/games",
                },
                {
                    title: "Collectibles",
                    href: "/collectibles",
                },
                {
                    title: "Videos",
                    href: "/videos",
                },
                {
                    title: "Fans",
                    href: "/fans",
                },
                {
                    title: "News",
                    href: "/news",
                }
            ],
            shopLinks: [
                {
                    title: "Shop DC",
                    href: "/shop"
                },
                {
                    title: "Shop DC Collectibles",
                    href: "/collectibles",
                }
            ],
            dcLinks: [
                {
                    title: "Terms of use",
                    href: "/terms of use",
                },
                {
                    title: "Privacy policy (new)",
                    href: "/privacypolicy",
                },
                {
                    title: "Ad choices",
                    href: "/adchoices",
                },
                {
                    title: "Advertising",
                    href: "/advertising",
                },
                {
                    title: "Jobs",
                    href: "/jobs",
                },
                {
                    title: "Subscriptions",
                    href: "/subscriptions",
                },
                {
                    title: "Talent workshops",
                    href: "/talentworkshops",
                },
                {
                    title: "CPSC Certificates",
                    href: "/certificates",
                },
                {
                    title: "Ratings",
                    href: "/ratings",
                },
                {
                    title: "Shop help",
                    href: "/shophelp",
                },
                {
                    title: "Contact us",
                    href: "/contactus",
                }
            ],
            sitesLinks:[
                {
                    title: "DC",
                    href: "/dc",
                },
                {
                    title: "MAD Magazine",
                    href: "/madmagazine",
                },
                {
                    title: "DC Kids",
                    href: "/dckids",
                },
                {
                    title: "DC Universe",
                    href: "/dcuniverse",
                },
                {
                    title: "DC Power Visa",
                    href: "/dcpowervisa",
                },
            ]
        }
    }
}

</script>

<template>
  <footer>
    <div class="top-footer">
        <div class="container">

            <div class="cols">
                <div class="col">
                    <h3>DC COMICS</h3>
                    <ul class="links">
                        <li v-for="(link, index) in dcComicsLinks" :key="index" class="link">
                            <a @click.prevent :href="link.href">{{link.title}}</a>
                        </li>
                    </ul>
                    <h3>SHOP</h3>
                    <ul class="links">
                        <li v-for="(link, index) in shopLinks" :key="index" class="link">
                            <a @click.prevent :href="link.href">{{link.title}}</a>
                        </li>
                    </ul>
                </div>

                <div class="col">
                    <h3>DC</h3>
                    <ul class="links">
                        <li v-for="(link, index) in dcLinks" :key="index" class="link">
                            <a @click.prevent :href="link.href">{{link.title}}</a>
                        </li>
                    </ul>
                </div>

                <div class="col">
                    <h3>SITES</h3>
                    <ul class="links">
                        <li v-for="(link, index) in sitesLinks" :key="index" class="link">
                            <a @click.prevent :href="link.href">{{link.title}}</a>
                        </li>
                    </ul>
                </div>

            </div>

            <div class="logo">                
                    <img src="../assets/img/dc-logo-bg.png" alt="DC Comics logo">
            </div>

        </div>
    </div>
    <div class="bot-footer">
        <div class="container">
            <button>SIGN-UP NOW</button>
            <div class="follow-us">
                <h3>FOLLOW US</h3>
                <img src="../assets/img/footer-facebook.png" alt="Facebook logo">
                <img src="../assets/img/footer-twitter.png" alt="Twitter logo">
                <img src="../assets/img/footer-youtube.png" alt="Youtube logo">
                <img src="../assets/img/footer-pinterest.png" alt="Pintarest logo">
                <img src="../assets/img/footer-periscope.png" alt="Periscope logo">
            </div>
        </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
// links
@use "../style/general.scss" as *;
@use "../style/partials/variables" as *;
// /links
footer{
    .top-footer{
        background-image: url(../assets/img/footer-bg.jpg);
        color: white;
        overflow: hidden;
        .container{
            display: flex;
            justify-content: space-between;
            padding: 2.5rem 0;
            .cols{
                display: flex;
                justify-content: flex-start;
                .col{
                    padding-right: 2rem;
                    h3{
                        padding-bottom: .7rem;
                    }
                    ul{
                        padding-bottom: .7rem;
                        li{
                            a{
                                color: white;
                                opacity: 0.3;
                                font-size: .9rem;
                                &:hover{
                                    opacity: 0.8;
                                }
                            }
                        }
                    }
                }
            }
            .logo{
                position: relative;
                height: 100%;
                width: 500px;
                img{
                    position: absolute;
                    top: -4rem;
                }
            }
            
        }
        
    }

    .bot-footer{
        background-color: $footer-bg;
        padding: 2rem 0;
        .container{
            display: flex;
            justify-content: space-between;
            button{
                background-color: $footer-bg;
                border: 2px solid $primary-color;
                padding: 1rem 2rem;
                color: white;
                font-weight: 700;
                &:hover{
                    background-color: $primary-color;
                    transition: all .5s;
                }
            }
            .follow-us{
                display: flex;
                gap: 1rem;
                align-items: center;
                color: $primary-color;
            }
        }
    }
}

</style>
