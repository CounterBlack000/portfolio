<template>
  <!--<TestPage />-->
  <LandingPage v-if="setPageDepth1 === 'LandingPage'" @toAIDevTestMain="toAIDevTestMain"/>
  <AIDevTestMain v-if="setPageDepth1 === 'AIDevTestMain'"/>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import LandingPage from '@/components/Landing/LandingPage.vue';
import AIDevTestMain from '@/components/openAITest/AIDevTestMain.vue';

//import TestPage from '@/components/Landing/TestPage.vue';

export default {
  name: 'App',
  components: {
    LandingPage,
    AIDevTestMain,
    //TestPage
  },
  data(){
    return{
      setPageDepth1: 'LandingPage'
    }
  },
  methods:{
    toAIDevTestMain(){
      this.setPageDepth1 = 'AIDevTestMain';
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  height: 100%;
  width: 100%;
}

html{
  height: 100%;
  width: 100%;
  
}
body{
  height: 100%;
  width: 100%;

  margin: 0;
}
</style>
