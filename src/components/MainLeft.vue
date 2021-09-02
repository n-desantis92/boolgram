<template>
    <div id="main-left" class="main-left">
        <main-left-top>

        </main-left-top>
    </div>
</template>

<script>
import MainLeftTop from './MainLeftTop.vue'
export default {
  components: { MainLeftTop },
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