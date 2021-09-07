<template>
    <div class="main-left-top">
        <div class="card-story" v-for="(storia ,i) in stories" :key="i">
            <div class="profilo">
                <img :src="storia.profile_picture" alt="Profilo">
            </div>
            <p>{{storia.profile_name}}</p>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'card-story',
    data() {
        
        return {
            stories: []
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
                font-size: 12px;
                color: #262626;
            }
        }
    }
</style>