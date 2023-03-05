<template>
    <div class="particles">
        <div id="particles-js">
            <div @click="toAIDevTestMain()">for AIDevTestMain</div>
            <!--<div class="lightSource1"></div>
            <div class="lightSource2"></div>-->
        </div>
        
    </div>
</template>
  
<script>
import 'particles.js';
import particlesJson from '@/components/Landing/particles.json';

export default {
    name:"LandingPage",
    mounted() {
        this.setPage();
    },
    methods:{
        setPage(){
            console.log('setPage ');
            window.particlesJS("particles-js", particlesJson);
        },
        toAIDevTestMain(){
            console.log('toAIDevTestMain');
            this.$emit('toAIDevTestMain');
        }
    }
}
</script>
  
<style lang="scss" scoped>
.particles{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;

    #particles-js {
        display: flex;
        justify-content: center;
        align-items: flex-end;
        height: 100%;
        width: 100%;

        /*background-color: gray;
        box-shadow:
        inset 60px 60px 60px #fff,*/
        background-color: #fff;
        //background-image: linear-gradient(0deg, #87CEEB 0%, #fff 20%);
        /*box-shadow: 
            inset 0 -60px 30px #87CEEB,
            inset 0 -60px 30px #fff;*/

        /*.lightSource1{
            position: absolute;
            
            width: 2px;
            height: 2px;
            //box-shadow: 0 0 60px 60px white;
            mix-blend-mode: hard-light;
            background: #4BA6C7;
            animation: lightShine1 5s infinite alternate;
        }

        .lightSource2{
            position: absolute;
            
            height: 7rem;
            width: 1px;

            transform: rotate( 10deg );

            //box-shadow: 10px 10px 150px 120px white;
            mix-blend-mode: hard-light;
            background: #4BA6C7;
            animation: lightShine2 5s infinite alternate;
        }*/

    }
}

/*@keyframes lightShine1{
    0%{
        box-shadow: 0 0 60px 10px #4BA6C7;
    }
    100%{
        box-shadow: 0 0 120px 10px #4BA6C7;
    }
}

@keyframes lightShine2{
    0%{
        box-shadow: 0 0 60px 30px #4BA6C7;
        opacity: 0.2;
    }
    100%{
        box-shadow: 0 0 120px 30px #4BA6C7;
        opacity: 0.5;
    }
}*/
</style>