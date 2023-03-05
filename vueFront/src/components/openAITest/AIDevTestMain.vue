<template>
    <div class="AIDevTestMain">
        <div class="opneAI">

        </div>
    </div>
</template>

<script>

export default{
    name: "AIDevTestMain",
    data(){
        return{
            test: 'data'
        }
    },
    mounted(){
        this.setVal();
    },
    methods:{
        async setVal(){
            console.log('AIDevTestMain set Page');
        }
    }
}
</script>

<style lang="scss" scoped>
.AIDevTestMain{
    display: flex;
    width: 100%;
    height: 100%;
}
</style>