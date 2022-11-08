<script>
import AppHeaderVue from './components/AppHeader.vue';
import AppMainVue from './components/AppMain.vue';
import AppFooterVue from './components/AppFooter.vue';
import AppJumboVue from './components/AppJumbo.vue';

export default{
  data(){
    return{

    }
  },
  components:{
    AppHeaderVue,
    AppMainVue,
    AppJumboVue,
    AppFooterVue
  },
}
</script>

<template>
  <AppHeaderVue />
  <AppMainVue />
  <AppJumboVue/>
  <AppFooterVue />
</template>

<style lang="scss">
// links
@use "./style/general.scss" as *;
@use "./style/partials/variables" as *;
// /links


</style>
