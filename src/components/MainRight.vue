<template>
    <div id="main-right" class="main-right">
        <main-right-top></main-right-top>
        <main-right-center></main-right-center>
        <main-right-bottom></main-right-bottom>
    </div>
</template>

<script>
import MainRightBottom from './MainRightBottom.vue'
import MainRightCenter from './MainRightCenter.vue'
import MainRightTop from './MainRightTop.vue'
export default {
  components: { MainRightTop, MainRightCenter, MainRightBottom },
    name: 'main-right',
    data() {
        
        return {
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .main-right {
        width: 20%;
        height: 100%;
        position: fixed;
        right: 20%;

    }
</style>