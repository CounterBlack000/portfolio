<template>
    <div class="water">
        <!--<div class="light"></div>-->
        <div class="underLight"></div>
    </div>
</template>

<script>
export default{
    name:"TestPage",
    mounted() {
      this.setVal();
    },
    methods:{
      setVal(){
        console.log('d');
      }
    }
}
</script>

<style lang="scss" scoped>
.water {
  position: relative;
  height: 200px;
  background-color: #4da6ff; /* blue color */
}

.light {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0;
  border-radius: 50%;
  box-shadow: 0 0 20px 10px rgba(255, 255, 255, 0.8); 
  animation: shine 2s infinite;
}

.underLight{
  position: absolute;
  bottom: 0;
  left: 0;
  width: 30%;
  height: 0;
  animation: underShine 5s infinite;
  //box-shadow: 0 0 20px 10px rgba(255, 255, 255, 0.8); 
}

@keyframes underShine{
  0%{
    box-shadow: 0 0 30px 50px rgba(255, 255, 255, 0.8); 
  }
  100%{
    box-shadow: 0 0 40px 70px rgba(255, 255, 255, 0.8); 
  }
}

@keyframes shine {
  0% {
    height: 0;
    opacity: 0.5;
  }
  50% {
    height: 100%;
    opacity: 1;
  }
  100% {
    height: 0;
    opacity: 0.5;
  }
}
</style>