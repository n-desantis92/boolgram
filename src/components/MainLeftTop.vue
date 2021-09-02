<template>
    <div id="main-left-top" class="main-left-top">
        <story-card>

        </story-card>
    </div>
</template>

<script>
import StoryCard from './StoryCard.vue'
export default {
  components: { StoryCard },
    name: 'main-left-top',
    data() {
        
        return {
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .main-left-top {
        background-color: #fff;
        width: 100%;
        height: 120px;
        border: 1px solid rgba(var(--b6a,219,219,219),1);
        border-radius: 3px;
        margin-top: 40px;
        padding: 10px 0;
    }
</style>