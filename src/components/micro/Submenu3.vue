<template>
  <div>
    <li>
        <a href="#">Support</a>
        <a href="#" @click="burger1()">
            <i class="fas fa-chevron-down" ></i>
        </a> 
        <div class="submenu"  :class="openMenu == false ? 'closed' : '' ">
            <ul>
                <li v-for="(support,index) in supports" :key="index">{{support}}</li>
            </ul>
        </div>
    </li>            
  </div>
</template>

<script>
export default {
    name:"Submenu3",
    data(){
        return{
              openMenu:false,
              supports:["support1","support2","support3"] ,
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