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
        <div class="post-bottom">
            <div class="cta">
                <i class="far fa-heart"></i>
                <i class="far fa-comment"></i>
                <i class="far fa-paper-plane"></i>
            </div>
            <div class="like">
                <div class="like-profilo">
                    <img src="@/assets/profile.jpg" alt="profilo">
                </div>
                Piace a <strong>Trudie35</strong> ed altri 4
            </div>
            <div class="comments">
                <strong>Stark.jace</strong> Queen of Hearts.
                <h5>Mostra tutti e 4 i commenti</h5>
                <strong>ciccio</strong> i get.
            </div>
            <div class="time">
                13 ore fa
            </div>
            <div class="add-comment">
                <i class="far fa-smile"></i>
                <input type="text" placeholder="Aggiungi un commento">
                <a href="#">pubblica</a>
            </div>
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
            img {
                width: 100%;
            }
        }
        .post-bottom {
            width: 100%;
            .cta {
                padding: 0 10px;
                font-size: 24px;
                i {
                    margin: 10px;
                    cursor: pointer;
                }
            }
            .like {
                padding: 0 20px;
                width: 100%;
                display: flex;
                align-items: center;
                margin: 5px 0;
                .like-profilo {
                    width: 5%;
                    margin-right: 10px;
                    img {
                        width: 100%;
                        border-radius: 50%;
                    }
                }
                strong {
                    margin: 0 5px;
                }
            }
            .comments {
                padding: 0 20px;
            }
            .time {
                padding: 10px 20px;
            }
            .add-comment {
                border-top: 1px solid rgba(var(--b6a,219,219,219),1);
                padding: 10px 0;
                width: 100%;
                display: flex;
                align-items: center;
                justify-content: space-between;
                i {
                    margin-left: 20px;
                    font-size: 24px;
                }
                input {
                    widows: 70%;
                    border: none;
                    outline: none;
                    margin: 0 10px;
                }
                a {
                    margin-right: 20px;
                    text-decoration: none;
                }
            }
        }
    }
</style>