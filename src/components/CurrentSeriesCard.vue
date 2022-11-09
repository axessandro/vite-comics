<script>
export default{
    name: "CurrentSeriesCard",
    props: {
        title: String,
        thumb: String,
    }
}
</script>

<template>
    <div class="card">
        <div class="img-wrapper">
            <img class="thumb" :src="thumb" :alt="title">
        </div>
        <p>{{title.toUpperCase()}}</p>
    </div>
</template>

<style lang="scss" scoped>
// links
@use "../style/general.scss" as *;
@use "../style/partials/variables" as *;
// /links
.card{
    width: calc(100% / 6 - 1.5rem);
    p{
        max-width: 100%;
        padding-top: 1rem;
        font-size: .8rem;
    }
    .img-wrapper{
        width: 100%;
        height: 250px;
        .thumb{
            height: 100%;
            width: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
}

</style>