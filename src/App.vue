<template>
  <div id="app">
    <Home-Header></Home-Header>
    <div class="maincontant">
     <router-view></router-view>
  </div>   
  </div>
</template>

<script>
import HomeHeader from './components/HomeHeader';

export default {
  components: {

  
    HomeHeader

  },
  name: 'App',
  methods:{
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      },
       goBack(){

                 //跳转到上一次浏览的界面
                 this.$router.go(-1)
 
                 //指定跳转的地址
                 // this.$router.replace('/menu')
 
                 //指定跳转路由的名字下
                 // this.$router.replace({name:'menuLink'})
 
                 //通过push进行跳转
                 // this.$router.push('/menu')
                // this.$router.push({name:'menuLink'})
             }
  
  }
}
</script>

<style>
/* @import "./font-awesome-4.7.0/css/font-awesome.min.css"; */
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
.maincontant{
   position:fixed;
   top:70px;
   left:220px;
   width:100%;
   height:100%;
   /* background-color:lightblue; */
}
</style>

