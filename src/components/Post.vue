<template>
    <div>
        <div class="post" v-for="(post,i) in posts" :key="i">
            <div class="post-top">
                <div class="cont-profilo">
                    <div class="profilo">
                        <img :src="post.profile_picture" alt="profilo">
                    </div>
                    <div class="name-profilo">
                        <h5>{{post.profile_name}}</h5>
                        <p>luogo</p>
                    </div>
                </div>
                <div class="option">
                    <i class="fas fa-ellipsis-h"></i>
                </div>
            </div>
            <div class="foto">
                <img :src="post.post_image" alt="foto">
            </div>
            <div class="post-bottom">
                <div class="cta">
                    <i class="far fa-heart"></i>
                    <i class="far fa-comment"></i>
                    <i class="far fa-paper-plane"></i>
                </div>
                <div class="like">
                    <div class="like-profilo">
                        <img :src="post.likes[0].profile_picture" alt="profilo">
                    </div>
                    Piace a <strong>{{post.likes[0].username}}</strong> ed altri 4
                </div>
                <div class="comments">
                    <strong>{{post.profile_fullname}}</strong> {{post.post_text}}
                    <div class="comment" v-for="(comment,y) in post.comments" :key="y">
                        <strong>{{comment.username}} </strong> {{comment.text}}
                    </div>
                    <h5>Mostra tutti e 4 i commenti</h5>
                    <strong>ciccio</strong> i get.
                </div>
                <div class="time">
                    {{getOra(post.date)}}
                </div>
                <div class="add-comment">
                    <i class="far fa-smile"></i>
                    <input type="text" placeholder="Aggiungi un commento">
                    <a href="#">pubblica</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
  
    name: 'post',
    data() {
        
        return {
            posts: [],
            data: new Date()
        }
    },
    props : {


    },created() {
        this.getPost();
    },
    methods: {
        getPost() {
            axios.get('https://flynn.boolean.careers/exercises/api/boolgram/posts')
            .then( (response) => {
                this.posts = response.data;
                console.log(response.data);
            })
            .catch(function (error) {
                console.log(error);
            });
        },
        getOra(data) {
            console.log(data);
            // const now = data;

            // let delta = parseInt((now.getTime() - date) / 1000, 10);
            // console.log(delta);
            // delta = delta + (now.getTimezoneOffset() * 60);

            // if(delta < 60) {
            //     return 'less than a minute ago';
            // }
            // if(delta < 120) {
            //     return 'about a minute ago';
            // }
            // if(delta < (60 * 60)) {
            //     return `${parseInt(delta / 60, 10).toString()} minutes ago`;
            // }
            // if(delta < (120 * 60)) {
            //     return 'about an hour ago';
            // }
            // if(delta < (24 * 60 * 60)) {
            //     return `about ${parseInt(delta / 3600, 10).toString()} hours ago`; 
            // }
            // if(delta < (48 * 60 * 60)) {
            //     return 'a day ago';
            // }

            // return `${parseInt(delta / 86400, 10).toString()} days ago`;

        }
    },
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
                    width: 40px;
                    height: 40px;
                    border-radius: 50%;
                    overflow: hidden;
                    cursor: pointer;
                    img {
                        height: 100%;
                        width: 100%;
                        object-fit: cover;
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
                    width: 30px;
                    height: 30px;
                    margin-right: 10px;
                    img {
                        height: 100%;
                        width: 100%;
                        object-fit: cover;
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