<script>
export default{
    name: "AppFooter",
}

</script>

<template>
  <footer>
    <div class="top-footer">
        <div class="container">
            <div class="col">
                
            </div>
        </div>
    </div>
    <div class="bot-footer">
        <div class="container">

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
        
    }
}

</style>
