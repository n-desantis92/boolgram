<template>
    <div id="card-story" class="card-story">
        <div class="profilo">
            <img src="@/assets/profile.jpg" alt="Profilo">
        </div>
        <p>{{nomeProfilo}}ciao</p>
    </div>
</template>

<script>
export default {
    name: 'card-story',
    data() {
        
        return {
        }
    },
    props : {

        nomeProfilo: String,
        fotoProfilo: String
    }
}
</script>

<style lang="scss">
    .card-story {
        width: calc(100% / 7.5);
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        .profilo {
            width: 70%;
            overflow: hidden;
            img {
                width: 100%;
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
</style>