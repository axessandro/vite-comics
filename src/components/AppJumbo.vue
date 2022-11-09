<script>
export default{
    name: "AppJumbo",
    data(){
        return{
            links: [
                {
                    img: "buy-comics-digital-comics.png",
                    title: "digital comics",
                    href: "/digitalcomics",
                },
                {
                    img: "buy-comics-merchandise.png",
                    title: "DC merchandise",
                    href: "/dcmerchandise",
                },
                {
                    img: "buy-comics-subscriptions.png",
                    title: "subscriptions",
                    href: "/subscriptions",
                },
                {
                    img: "buy-comics-shop-locator.png",
                    title: "comic shop locator",
                    href: "/comicshoplocator",
                },
                {
                    img: "buy-dc-power-visa.svg",
                    title: "dc power visa",
                    href: "/dcpowervisa",
                },
            ]
        }
    },
    methods: {
        getImagePath(imgPath){
            return new URL(imgPath, import.meta.url).href
        }
    }
}
</script>

<template>
  <div class="jumbo">
    <div class="container">
        <ul class="links">
            <li v-for="(link, index) in links" :key="index" class="link">
                <img :src="getImagePath(`../assets/img/${link.img}`)" alt="">
                <a @click.prevent :href="link.href">{{link.title.toUpperCase()}}</a>
            </li>
        </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
// links
@use "../style/general.scss" as *;
@use "../style/partials/variables" as *;
// /links
.jumbo{
    background-color: $primary-color;
    padding: 2rem 0;
    .container{
        ul{
            display: flex;
            justify-content: space-between;

            li{
                display: flex;
                align-items: center;

                &:last-child img{
                    height: auto;
                    width: 50px;
                }

                img{
                    height: 50px;
                    margin-right: .7rem;
                }
                a{
                    color: white;
                    font-size: .8rem;

                }
            }
        }
    }
}

</style>
