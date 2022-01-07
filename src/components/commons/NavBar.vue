<template>
  <nav>
      <Logo/>
      <Menu/>
  </nav>
</template>

<script>
import Logo from "../partials/Logo.vue";
import Menu from "../partials/Menu.vue";
export default {
    name:"NavBar",
    components:{
        Logo,
        Menu,
    }
}
</script>

<style lang="scss" scoped>
    nav{
        display: flex;
        align-items: center;
        height:100%;
        width: 95%;
        margin:auto;
        background-color:white;
    }
</style>