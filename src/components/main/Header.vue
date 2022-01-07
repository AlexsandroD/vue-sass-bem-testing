<template>
  <header>
    <NavBar/>
  </header>
</template>

<script>
import NavBar from "../commons/NavBar.vue";
export default {
    name:"Header",
    components:{
        NavBar,
    }
}
</script>

<style lang="scss" scoped>
    header{
        height: 80px;
        background-color: white;
    }
</style>