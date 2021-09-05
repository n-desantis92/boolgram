<template>
    <div id="main-left" class="main-left">
        <main-left-top>

        </main-left-top>
        <post></post>
    </div>
</template>

<script>
import MainLeftTop from './MainLeftTop.vue'
import Post from './Post.vue'
export default {
  components: { MainLeftTop, Post },
    name: 'main-left',
    data() {
        
        return {
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .main-left {
        width: 65%;
        height: 100%;
    }
</style>