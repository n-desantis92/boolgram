<template>
    <div id="profilo-suggerito" class="content-sug">
        <div class="cont-profilo">
            <div class="profilo">
                <img src="@/assets/profile.jpg" alt="profilo">
            </div>
            <div class="name-profilo">
                <h5>nome profilo</h5>
                <p>nome</p>
            </div>

        </div>
        <div class="cont-seg"><a href="#">Segui</a></div>
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


    }
}
</script>

<style lang="scss">

    .content-sug {
        width: 100%;
        height: calc(100% / 5);
        display: flex;
        justify-content: space-between;
        align-items: center;
        .cont-profilo {
            width: 70%;
            height: 70%;
            display: flex;
            align-items: center;
            padding-left: 10px;
            .profilo {
                width: 18%;
                overflow: hidden;
                cursor: pointer;
                img {
                    width: 100%;
                    border-radius: 50%;
                    padding: 1px;
                }
            }

            .name-profilo {
                margin-left: 20px;
                h5 {
                    font-size: 16px;
                }

            }
        }
        .cont-seg {
            a {
                text-decoration: none;
            }
        }
    }
</style>
