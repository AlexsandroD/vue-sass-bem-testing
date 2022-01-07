<template>
  <div>
    <li>
        <a href="#">Products</a>
        <a href="#" @click="burger1()">
            <i class="fas fa-chevron-down" ></i>
        </a> 
        <div class="submenu"  :class="openMenu == false ? 'closed' : '' ">
            <ul>
                <li v-for="(product,index) in products" :key="index">{{product}}</li>
            </ul>
        </div>
    </li>            
  </div>
</template>

<script>
export default {
    name:"Submenu",
    data(){
        return{
              openMenu:false,
              products:["prduct1","prduct2","prduct3","prduct4"] ,
        }
    },



    methods:{
           burger1:function(){
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

</style>