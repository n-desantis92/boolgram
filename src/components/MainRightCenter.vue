<template>
    <div id="main-right-center" class="main-right-center">
        <div class="center-top">
        <h4>Suggerimenti per te</h4>
        <p>Mostra tutti</p>
        </div>
        <div class="suggerimenti">
            <profilo-suggerito></profilo-suggerito>
        </div>
    </div>
</template>

<script>
import ProfiloSuggerito from './Profilo-suggerito.vue'
export default {
  components: { ProfiloSuggerito },
    name: 'main-right-center',
    data() {
        
        return {
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .main-right-center {
        background-color: rgb(255, 0, 0);
        width: 100%;
        height: 50%;

        .center-top {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
            h4 {
                color: grey;
            }
        }
        .suggerimenti {
            padding-top: 10px;
        }
    }
</style>