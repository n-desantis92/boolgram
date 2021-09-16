<template>
    <div class="container-skel" v-show="loading">

        <div class="main">
            <div class="left">
                <div class="load">
                    <img src="@/assets/spinner.gif">
                </div>
                <div class="storyes">
                    <div v-for="(storia, i) in 7" :key="i" class="circle pulse"></div>
                </div>
                <div class="post wave">
                    <div class="post-top">
                        <div class="circle pulse"></div>
                        <div class="cont-rect">
                            <div class="rectangle pulse"></div>
                            <div class="rectangle pulse small"></div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="right">
                <main-right-top></main-right-top>
                <!-- centro suggeriti -->
                <div class="main-right-center">
                    <div class="title-right">
                        <h4>Suggeriti per te</h4>
                        <strong>mostra tutti</strong>
                    </div>
                    <!-- suggerito -->
                    <div class="suggerito" v-for="(suggerito,i) in 5" :key="i">
                        <div class="circle pulse"></div>
                        <div class="cont-rect">
                            <div class="rectangle pulse"></div>
                            <div class="rectangle pulse small"></div>
                        </div>
                    </div>
                </div>
                <main-right-bottom></main-right-bottom>
            </div>
        </div>
    </div>
</template>

<script>
import MainRightBottom from './MainRightBottom.vue';
import MainRightTop from './MainRightTop.vue';

export default {
    name: 'SkeletonLoader',
    components : {
        MainRightTop,
        MainRightBottom
    },
    data() {
        return {
            loading: true
        }
    },
    mounted() {
      setTimeout(() => {
          this.setLoadingState(false)
      },5000)
    },
    methods: {
        setLoadingState(value){
            this.loading = value;
        }
    },

}
</script>

<style lang="scss">
    .container-skel{
        background: rgba(var(--b3f,250,250,250),1);
        height: 100vh;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: fixed;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;

        .circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            margin: 0 10px;
        }
        .cont-rect {
            margin-left: 10px;

            .rectangle {
                width: 150px;
                height: 12px;
                margin-bottom: 5px;
            }
            .small {
                width: 80px;
            }
        }
        .main {
            height: 100vh;
            width: 100%;
            display: flex;
            justify-content: center;



            .left {
                position: relative;
                width: 40%;
                height: 100vh;
                display: flex;
                flex-direction: column;
                margin-right: 20px;
                text-align: center;
                .load {
                    width: 40px;
                    position: absolute;
                    top: 60px;
                    left: 50%;
                    transform: translateX(-50%);
                    z-index: 50;
                    img {
                        width: 100%;
                    }
                }
                .storyes {
                    width: 100%;
                    height: 120px;
                    border: 1px solid rgba(var(--b6a,219,219,219),1);
                    border-radius: 3px;
                    margin-top: 100px;
                    display: flex;
                    justify-content: flex-start;
                    align-items: center;
                    overflow: hidden;
                    padding: 10px;
                    background-color: #fff;

                }
                .post{
                    width: 100%;
                    height: 400px;
                    .post-top{
                        height: 60px;
                        width: 100%;
                        display: flex;
                        justify-content: flex-start;
                        align-items: center;
                        & div.circle {
                            width: 45px;
                            height: 45px;
                        }

                    }
                }
            }
            .right {
                width: 20%;
                height: 100%;
                padding-top: 20px;
                .main-right-center {
                    display: flex;
                    flex-direction: column;
                    margin-top: 30px;
                    .title-right {
                        display: flex;
                        justify-content: space-between;
                        font-size: 13px;
                        margin-bottom: 20px;
                        h4 {
                            color: rgb(162, 162, 162);
                        }
                    }

                    .suggerito {
                        display: flex;
                        align-items: center;
                        margin-top: 10px;
                        & div.circle {
                            width: 50px;
                            height: 50px;
                        }                       
                    }
                }
            }
        }
    
    }
    // animazioni
    .wave {
        animation: wave 1s infinite linear forwards;
        -webkit-animation: wave 1s infinite linear forwards;
        background: #f6f7f8;
        background: linear-gradient(to right, #eeeeee 8%, #dddddd 18%, #eeeeee 33%);
        background-size: 800px 104px;
    }
    @keyframes wave {
        0% {
            background-position: -468px 0
        }
        100% {
            background-position: 468px 0
        }
    }

    .pulse {
        animation: pulse 1s infinite ease-in-out;
        -webkit-animation: pulse 1s infinite ease-in-out;
    }
    @keyframes pulse {
        0% {
        background-color: rgba(165, 165, 165, .1);
                }
        50% {
        background-color: rgba(165, 165, 165, .3);
                }
        100% {
        background-color: rgba(165, 165, 165, .1);
                }
    }
    @-webkit-keyframes pulse {
        0% {
        background-color: rgba(165, 165, 165, .1);
                }
        50% {
        background-color: rgba(165, 165, 165, .3);
                }
        100% {
        background-color: rgba(165, 165, 165, .1);
                }
    }
</style>