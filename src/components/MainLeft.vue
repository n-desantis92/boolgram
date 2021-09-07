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
import axios from 'axios'

export default {
  components: { MainLeftTop, Post },
    name: 'main-left',
    props : {

    },
    data() {
        return {
            stories: [],
        }
    },
    methods: {
        setStories(){
            axios.get('https://flynn.boolean.careers/exercises/api/boolgram/profiles')
            .then( (response) => {
                this.stories = response.data;
                console.log(response.data);
            })
            .catch(function (error) {
                console.log(error);
            });
        },
    },

}
</script>

<style lang="scss">
    .main-left {
        width: 65%;
        height: 100%;
    }
</style>