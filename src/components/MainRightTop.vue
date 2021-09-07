<template>
    <div id="main-right-top" class="main-right-top">
        <div class="cont-profilo">
            <div class="profilo">
                <img src="@/assets/profile.jpg" alt="profilo">
            </div>
            <div class="name-profilo">
                <h5>{{profilo.username}}</h5>
                <p>{{profilo.name}}</p>
            </div>
        </div>

        <div class="suggerimenti">
            <a href="#">passa a</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'main-right-top',
    props : {

    },
    data() {
        
        return {
            profilo: {
                name: 'Nicolas De santis',
                username: 'dsn'
            }
        }
    },


}
</script>

<style lang="scss">

    .main-right-top {
        width: 100%;
        display: flex;
        align-items: center;
        margin-top: 35%;


        .cont-profilo {
            width: 70%;
            height: 70%;
            display: flex;
            align-items: center;
            padding-left: 10px;
            .profilo {
                width: 30%;
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
                p {
                    font-size: 14px;
                }

            }
        }
        .suggerimenti {
            width: 30%;
            display: flex;
            justify-content: center;
            align-items: center;
            a {
                text-decoration: none;
            }
        }
    }
    
</style>