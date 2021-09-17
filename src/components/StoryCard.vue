<template>
    <div class="main-left-top">
        <div class="card-story" v-for="(storia ,i) in stories" :key="i">
            <div class="profilo" v-on:click="openStoryMode(i)">
                <img :src="storia.profile_picture" alt="Profilo">
            </div>
            <p>{{storia.profile_name}}</p>
        </div>
        <div class="story" v-show="openStory">
            <div class="logo">
                <img src="@/assets/logo-white.png" alt="logo boolgram">
            </div>
            <div class="close" v-on:click="closeStory()">
                <i  class="fas fa-times-circle" id="close"></i>
            </div>
            <div class="arrow" v-on:click="prevStory()">
                <i class="fas fa-chevron-circle-left"></i>
            </div>
            <div class="cont-img">
                <img :src="pictures[index]">              
            </div>
            <div class="arrow" v-on:click="nextStory()">
                <i class="fas fa-chevron-circle-right"></i>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'card-story',
    data() {
        
        return {
            stories: [],
            pictures: [
                'https://i.pinimg.com/originals/74/f4/4a/74f44a7a0d5fa2a52cb2c00d311fdb38.jpg',
                'https://i.pinimg.com/564x/e9/34/f4/e934f42f1240da8717c9333055a331a0.jpg',
                'https://gobrand.it/wp-content/uploads/2019/10/1571312472963-576x1024.jpg',
                'https://xoxobella.com/wp-content/uploads/2020/06/instagram_captions_for_selfies_and-_selfie_puns_bella_bucchiotti-5.jpg',
                'https://i1.wp.com/www.thegiornale.it/wp-content/uploads/2018/08/pose-perfette-per-instagram-tc.jpeg?resize=800%2C1132&ssl=1',
                'https://static2-viaggi.corriereobjects.it/wp-content/uploads/2020/01/2.jpeg?v=364319',
                'https://i2.wp.com/www.thegiornale.it/wp-content/uploads/2020/04/come-fare-foto-perfette-per-instagram.jpg?resize=564%2C564&ssl=1'
            ],
            openStory: false,
            index: null,
        }
    },
    created() {
        this.getstories();
    },
    methods: {
        getstories() {
            axios.get('https://flynn.boolean.careers/exercises/api/boolgram/profiles')
            .then( (response) => {
                this.stories = response.data;
                console.log(response.data);
            })
            .catch(function (error) {
                console.log(error);
            });
        },
        closeStory() {
            this.openStory = false;
        },
        openStoryMode(indice) {
            this.openStory = true;
            this.index = indice;
        },
        nextStory() {
            if (this.index == (this.pictures.length - 1)) {
                this.index = 0;
            }else if (this.index < this.pictures.length) {
                this.index ++;
            }
        },
        prevStory() {
            if (this.index == 0) {
                this.index = (this.pictures.length - 1);
            }else if (this.index <= this.pictures.length) {
                this.index --;
            }
        }
        
    },
}
</script>

<style lang="scss">

        .main-left-top {
        background-color: #fff;
        width: 100%;
        height: 120px;
        border: 1px solid rgba(var(--b6a,219,219,219),1);
        border-radius: 3px;
        margin-top: 85px;
        display: flex;
        flex-wrap: wrap;
        overflow: hidden;
        padding: 0;
        
        .card-story {
            width: calc(100% / 7.5);
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            .profilo {
                width: 60px;
                height: 60px;
                overflow: hidden;
                border-radius: 50%;
                img {
                    height: 100%;
                    width: 100%;
                    object-fit: cover;
                    border: 3px solid red;
                    border-radius: 50%;
                    padding: 1px;
                }
            }

            p {
                width: 100%;
                font-size: 12px;
                color: #262626;
                text-align: center;
                text-overflow: ellipsis;
                overflow: hidden;
            }
        }
        .story {
            position: fixed;
            z-index: 150;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-color: black;
            display: flex;
            justify-content: center;
            align-items: center;

            .logo {
                width: 150px;
                position: absolute;
                left: 20px;
                top: 20px;
                img {
                    width: 100%;
                    color: #fff;
                }
            }
            .arrow {
                font-size: 22px;
                color: #fff;
                cursor: pointer;
                margin: 20px;
            }
            .cont-img {
                width: 30%;
                height: 90%;
                border-radius: 10px;
                overflow: hidden;
                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }
            }
            .close {
                width: 20px;
                height: 20px;
                position: absolute;
                right: 20px;
                top: 20px;

                i {
                    color: #fff;
                    font-size: 20px;
                    cursor: pointer;
                }
            }
        }
    }
</style>