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
                active: false,
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
        
            if (this.links[index].active === false) {
                this.links[index].active === true
            }else{
                this.links[index].active === false
            }  
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
                <li v-for="(link, index) in links" :key="index" class="link" @click.prevent="toggleActive(index)">
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
    padding: 1rem 0;
    color: $primary-color;
    font-size: 1rem;
    font-weight: 500;
    .container{
        display: flex;
        justify-content: space-between;
    
        .logo{
            min-width: 150px;
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
            }
            .active{
                color: $primary-color;
                border-bottom: 2px solid black;
            }
        }
    
    }

}

</style>
