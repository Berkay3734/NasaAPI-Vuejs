<template>
  <WelcomePlanet v-if="showWelcomeScreen" />
  <ListWrapper v-else />
</template>

<script>
import ListWrapper from './components/ListWrapper.vue';
import WelcomePlanet from './components/WelcomePlanet.vue';


export default {
  name: 'App',
  data(){
    return{
      showWelcomeScreen:false
    }
  },
  created(){
    setTimeout(()=>{
        document.body.style.padding="20px"
        document.body.style.overflow="auto"
        this.showWelcomeScreen=false
    },0)
  },
  components: {
    WelcomePlanet,
    ListWrapper
}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap');

::-webkit-scrollbar {
  width: 4px;
}
::-webkit-scrollbar-track {
  background: #0b3d91;
}
::-webkit-scrollbar-thumb {
  background: #fc3d21;
}
::-webkit-scrollbar-thumb:hover {
  background: #0b3d91;
}

body{
  font-family: 'Roboto', sans-serif;
  margin: 0;
  background-color: #0b3d91;
  overflow: hidden;
}
</style>
