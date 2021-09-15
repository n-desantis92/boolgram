<template>
    <div id="main-right-center" class="main-right-center">
        <div class="center-top">
        <h4>Suggerimenti per te</h4>
        <p>Mostra tutti</p>
        </div>
        <div class="suggerimenti">
            <profilo-suggerito :suggeriti ="this.suggeriti"></profilo-suggerito>
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
            suggeriti: [
                {
                    nome: 'Alvaro',
                    nik: 'Soler',
                    foto: 'https://www.camicissima.it/media/mageplaza/blog/post/c/a/camicissima_blog_trendy.jpg'
                },
                {
                    nome: 'raimondo',
                    nik: 'vianello',
                    foto: 'https://biografieonline.it/img/bio/Raimondo_Vianello_1.jpg'
                },
                {
                    nome: 'Jessica',
                    nik: 'Alba',
                    foto: 'https://www.amica.it/wp-content/uploads/2021/04/jessica-alba-oggi-GettyImages-1205621380.jpg'
                },
            ]
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .main-right-center {
        width: 100%;
        height: 50%;

        .center-top {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
            h4 {
                color: rgb(162, 162, 162);
            }
        }
        .suggerimenti {
            padding-top: 10px;
        }
    }
</style>