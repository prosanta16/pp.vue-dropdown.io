<template>
  <nav>
    <div class="menu-item"><a href="#">Home</a></div>
    <div class="menu-item"><a href="#">About</a></div>
    <Dropdown title="Servies" :item="services" />
    <div class="menu-item"><a href="#">Contact</a></div>
  </nav>

</template>

<script>
import Dropdown from './Dropdown';
export default {
  name:'navbar',
  components:{
    Dropdown
  },
  data(){
    return{
      services:[
        {
          title:'Web',
          link:'#'
        },
        {
          title:'Graphics',
          link:'#'
        },
        {
          title:'Android',
          link:'#'
        }
      ]
    }
  }
}
</script>

<style scoped>
  nav{
    display:flex;
    align-items:center;
    justify-content:center;
  }
  nav .menu-item{
    color:#FFF;
    padding:10px 20px;
    position:relative;
    text-align:center;
    border-bottom:3px solid transparent;
    display:flex;
    transition:0.4s;
  }
  nav .menu-item.active,
  nav .menu-item:hover{
    background-color:green;
    border-bottom-color:#FF5858;

  }

  nav .menu-item a{
    color:inherit;
    text-decoration:none;
  }
</style>
