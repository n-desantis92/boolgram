<template>
    <div id="main-right" class="main-right">
        <main-right-top></main-right-top>
        <main-right-center></main-right-center>
    </div>
</template>

<script>
import MainRightCenter from './MainRightCenter.vue'
import MainRightTop from './MainRightTop.vue'
export default {
  components: { MainRightTop, MainRightCenter },
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
        background-color: rgb(194, 194, 194);
        width: 20%;
        height: 100%;
        position: fixed;
        right: 20%;

    }
</style>