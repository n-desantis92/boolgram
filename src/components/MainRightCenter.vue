<template>
    <div id="main-right-center" class="main-right-center">
        <div class="center-top">
        <h4>Suggerimenti per te</h4>
        <p>Mostra tutti</p>
        </div>
    </div>
</template>

<script>
export default {
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
    }
</style>