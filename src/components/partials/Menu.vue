<template>
 <menu>
     <div class="burger-manu">
         <a class="icon-burger" @click="burger()"><i class="fas fa-bars"></i></a>
         <div class="hidden-menu" :class="openMenu == false ? 'closed' : '' ">
            <ul>
                <Submenu/>
                <li><a href="#">Custumers</a></li>
                <Submenu2/>
                <li><a href="#">Pricing</a></li>
            </ul>
            <ul>
                <li><a href="#">Docs</a></li>
                <Submenu3/>
                <li><a href="#">Login</a></li>
            </ul>
         </div>
     </div>
 </menu>
</template>

<script>
import Submenu from "../micro/Submenu.vue";
import Submenu2 from "../micro/Submenu2.vue";
import Submenu3 from "../micro/Submenu3.vue";
export default {
    name:"Menu",
    components:{
        Submenu,
        Submenu2,
        Submenu3,
    },
    data(){
        return{
            openMenu:false,     
        }
    },
    methods:{
        burger:function(){
            if(this.openMenu == false){
                this.openMenu = true;
            }else{
                this.openMenu = false;
            }
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/global.scss";
    menu{
        .burger-menu{
            position:relative;
        }
            .hidden-menu{
                position: absolute;
                right: 5rem;
                min-width: 100px;
                background-color: white;
            }
     
    }
    
</style>