<template>

  <div id="app">
    <img src="./assets/logo.png" >    
    <transition name = "bounce" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>

</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
*{margin: 0;border:0;}
#box{
width:100%;
height: 100vh;
overflow: hidden;
background:#000;
outline:1px solid red;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50; 
  width:100%;
  height: 100vh;
  overflow: hidden;
  outline:1px solid red;
  
}
.info-enter,.info-leave-active{
  opacity: 0;
  transform: translate3d(0,20%,0);
}
.info-leave-active,.info-enter-active{
  transform: all .5s cubic-border(0.4,0,0,1.5);
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .9s;  
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
  font-size: 36px;
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active for <2.1.8 */ {
  transform: translateX(100px);
  opacity: 0;
}


.bounce-enter-active {
  animation: bounce-in .5s;
}
.bounce-leave-active {
  animation: bounce-in .5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
</style>
