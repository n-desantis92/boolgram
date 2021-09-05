<template>
    <div id="post" class="post">
        <div class="post-top">
            <div class="cont-profilo">
                <div class="profilo">
                <img src="@/assets/profile.jpg" alt="profilo">
                </div>
                <div class="name-profilo">
                    <h5>nome</h5>
                    <p>luogo</p>
                </div>
            </div>
            <div class="option">
                <i class="fas fa-ellipsis-h"></i>
            </div>
        </div>
        <div class="foto">
            <img src="@/assets/profile.jpg" alt="foto">
        </div>
    </div>
</template>

<script>
export default {
  
    name: 'post',
    data() {
        
        return {
        }
    },
    props : {


    }
}
</script>

<style lang="scss">
    .post {
        width: 100%;
        height: 600px;
                background-color: #fff;
        border: 1px solid rgba(var(--b6a,219,219,219),1);
        border-radius: 3px;
        margin-top: 30px;

        .post-top {
            height: 60px;
            width: 100%;
            background-color: #fff;
            display: flex;
            justify-content: space-between;

            .cont-profilo {
                background-color: rgb(34, 255, 0);
                width: 30%;
                height: 100%;
                display: flex;
                align-items: center;
                padding-left: 10px;
                .profilo {
                    width: 25%;
                    overflow: hidden;
                    cursor: pointer;
                    img {
                        width: 100%;
                        border: 3px solid red;
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

            .option {
                display: flex;
                align-items: center;
                justify-content: center;
                i {
                    margin-right: 10px;
                    font-size: 16px;
                    cursor: pointer;
                }
            }
        }
        .foto {
            width: 100%;
            height: 716px;
            img {
                width: 100%;
            }
        }
    }
</style>