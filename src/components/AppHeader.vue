<script>
export default{
    name: "AppHeader",
    data(){
        return{
            links: [
            {
                title: "characters",
                href: "/characters",
                active: false,
            },
            {
                title: "comics",
                href: "/comics",
                active: true,
            },
            {
                title: "movies",
                href: "/movies",
                active: false,
            },
            {
                title: "tv",
                href: "/tv",
                active: false,
            },
            {
                title: "games",
                href: "/games",
                active: false,
            },
            {
                title: "collectibles",
                href: "/collectibles",
                active: false,
            },
            {
                title: "videos",
                href: "/videos",
                active: false,
            },
            {
                title: "fans",
                href: "/fans",
                active: false,
            },
            {
                title: "news",
                href: "/news",
                active: false,
            },
            {
                title: "shop",
                href: "/shop",
                active: false,
            }
            ]
        }
    },
    methods: {
        toggleActive(index){
            for ( let i = 0; i < this.links.length; i++){
                const link = this.links[i];
                link.active = false;
            }
            this.links[index].active = true;
            
        },
    }
}
</script>

<template>

  <header>
    <div class="container">
        <div class="logo"><img src="../assets/img/dc-logo.png" alt="DC Comics logo"></div>
        <nav>
            <ul class="links">
                <li v-for="(link, index) in links" :key="index" class="link" :class=" link.active === true ? 'active' : ''" @click.prevent="toggleActive(index)">
                    <a :href="link.href">{{link.title.toUpperCase()}}</a>
                </li>
            </ul>
        </nav>
    </div>
  </header>

</template>

<style lang="scss" scoped>
// links
@use "../style/general.scss" as *;
@use "../style/partials/variables" as *;
// /links
header{
    width: 100%;
    color: $primary-color;
    font-size: 1rem;
    font-weight: 500;
    
    .container{
        display: flex;
        justify-content: space-between;
        
        .logo{
            padding: 0.5rem 0;
            width: 80px;
        }

        ul{
            display: flex;
            align-items: center;
            height: 100%;

            li{
                padding: 0 0.8rem;
                height: 100%;
                display: flex;
                align-items: center;
                border-bottom: 8px solid #ffffff00;
                border-top: 8px solid #ffffff00;
                font-size: .8rem;
            }
            
            li.active{
                border-bottom: 8px solid $primary-color;
                a{
                    color: $primary-color;
                }
            }
        }
    }
}
</style>
