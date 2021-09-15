<template>
    <div id="profilo-suggerito" class="content-sug">
        <div class="cont-profilo" v-for="(suggerito,i) in this.suggeriti" :key="i">
            <div class="profilo">
                <img :src="suggerito.foto" alt="profilo">
            </div>
            <div class="name-profilo">
                <h5>{{suggerito.nik}}</h5>
                <p>{{suggerito.nome}}</p>
            </div>
            <div class="cont-seg"><a href="#">Segui</a></div>
        </div>
        
    </div>
</template>

<script>

export default {
    name: 'profilo-suggerito',
    data() {
        
        return {
        }
    },
    props : {

        suggeriti: Array
    }
}
</script>

<style lang="scss">

    .content-sug {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        .cont-profilo {
            position: relative;
            justify-content: flex-start;
            align-items: center;
            width: 100%;
            height: 60px;
            display: flex;
            align-items: center;
            padding-left: 10px;
            .profilo {
                width: 18%;
                height: 80%;
                overflow: hidden;
                cursor: pointer;
                img {
                    height: 100%;
                    width: 100%;
                    padding: 1px;
                    border-radius: 50%;
                    object-position: center;
                    object-fit: cover;
                }
            }

            .name-profilo {
                margin-left: 20px;
                h5 {
                    font-size: 16px;
                }

            }
            .cont-seg {
                position: absolute;
                right: 0;
                margin: 10px;
                a {
                    text-decoration: none;
                }
            }
        }
    }
</style>
