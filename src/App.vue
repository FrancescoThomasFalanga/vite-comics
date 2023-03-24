<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppUpperFooter from "./components/AppUpperFooter.vue";
import AppBottomFooter from "./components/AppBottomFooter.vue";

export default {
  data() {
    return {

    }
  },

  components: {
    AppNavbar,
    AppHeader,
    AppMain,
    AppUpperFooter,
    AppBottomFooter,
  }
}
</script>


<template>
  <div>

    <AppNavbar></AppNavbar>

    <AppHeader></AppHeader>

    <AppMain></AppMain>

    <AppUpperFooter></AppUpperFooter>

    <AppBottomFooter></AppBottomFooter>

  </div>
</template>


<style lang="scss" scoped>

</style>