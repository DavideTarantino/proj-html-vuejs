<script>
    export default {
        name: 'PageFooter',
        data(){
            return{
                recentPosts: [
                    {
                        link: '> The best protein shake'
                    },
                    {
                        link: '> Ultimate cardio workout'
                    },
                    {
                        link: '> New juices available now'
                    },
                    {
                        link: '> Tips to find trining partners'
                    },
                    {
                        link: '> 20 best healty recipes'
                    },
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section id="left">
            <div>
                <img src="../../../public/Imgaes/logo-200x34.png" alt="">
                <p>Ac aliquam neque sagittis diam faucibus vitae purus turpis phasellus. Pellentesque consectetur amet purus ultrices mauris.</p>
                <div id="loghi">
                    <span><i class="fa-brands fa-facebook-f" style="color: #FF414B;"></i></span>
                    <span><i class="fa-brands fa-x-twitter" style="color: #FF414B;"></i></span>
                    <span><i class="fa-brands fa-instagram" style="color: #FF414B;"></i></span>
                    <span><i class="fa-brands fa-youtube" style="color: #FF414B;"></i></span>
                    <span><i class="fa-brands fa-linkedin-in" style="color: #FF414B;"></i></span>
                </div>
            </div>
        </section>
        <section id="center">
            <div>
                <h2>RECENT POSTS</h2>
                <ul v-for="(element,index) in recentPosts" :key="index">
                    <li><a href="#">{{ element.link }}</a></li>
                </ul>
            </div>
        </section>
        <section id="right">
            <div>
                <h1>CONTACT INFORMATIONS</h1>
                <h2>4746 Tipple Road Michigan 48449</h2>
                <h3>Mobile: 1.800.000.0000</h3>
                <h3>Email: info@your-company.com</h3>
            </div>
        </section>
    </main>
    <hr>
    <footer>
        <span class="gray">© Copiright 2012 - 2024|</span> <a href="#">Avada Website Builder </a> <span class="gray">by</span> <a href="#">ThemeFusion</a> <span class="gray">|All Rights Reserved | Powered by</span> <a href="#">WorldPress</a>
    </footer>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
       background-color: black;
       display: flex;
       justify-content: space-between;
       height: 60vh;

       section{
        @include page-layout;
        padding-top: 7%;
       }

       #left{

        div{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            img{
                width: 35%;
            }
            p{
                margin-top: 20px;
                color: white;
                width: 65%;
                text-align: center;
                font-size: 17px;
                font-weight: 300;
                line-height: 29px;
            }

            #loghi{
                display: flex;
                margin-top: 30px;
                flex-direction: row;
                gap: 10px;
                cursor: pointer;
                font-size: 18px;
            }
        }
       }

       #center{
        color: white;

        div{
            display: flex;
            flex-direction: column;
            align-items: center;

            h2{
                margin-bottom: 30px;
            }

            ul{
                list-style-type: none;
                line-height: 40px;
                
                li{
                    a{
                        text-decoration: none;
                        color: white;
                        font-weight: 300;
                    }
                }
            }
        }
        
       }

       #right{
        color: white;

        div{
            display: flex;
            flex-direction: column;
            align-items: center;

            h1{
                margin-bottom: 40px;
            }
            h2{
                font-weight: 300;
                font-size: 22px;
                margin-bottom: 25px;
            }
        }
       }
    }

    footer{
        height: 10vh;
        background-color: black;
        color: white;
        display: flex;
        align-items: center;
        justify-content: center;
        .gray{
            color: gray;
        }

        a{
            padding-inline: 5px;
            text-decoration: none;
            color: white;
        }

        a:hover{
            color: #94CCFF;
        }
    }
</style>