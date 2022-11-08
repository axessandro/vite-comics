<script>
export default{
    name: "AppMain",
    
}
</script>

<template>
  <main>
    <div class="container">
        <h2>Content goes here </h2>
    </div>
  </main>
</template>

<style lang="scss" scoped>
// links
@use "../style/general.scss" as *;
@use "../style/partials/variables" as *;
// /links
main{
    background-color: $main-black;
    color: white;
    padding: 2rem 0;
}

</style>
