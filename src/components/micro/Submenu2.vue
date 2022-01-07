<template>
  <div>
    <li>
        <a href="#">Community</a>
        <a href="#" @click="burger()">
            <i class="fas fa-chevron-down" ></i>
        </a> 
        <div class="submenu"  :class="openMenu == false ? 'closed' : '' ">
            <ul>
                <li v-for="(community,index) in communities" :key="index">{{community}}</li>
            </ul>
        </div>
    </li>            
  </div>
</template>

<script>
export default {
    name:"Submenu2",
    data(){
        return{
              openMenu:false,
              communities:["community1","community2","community3","community4"],
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

</style>