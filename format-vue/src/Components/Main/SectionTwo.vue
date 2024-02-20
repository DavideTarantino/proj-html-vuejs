<script>
    export default {
        name: 'SectionTwo',
        data(){
            return{
                cards:[
                    {
                        imgUrl: '../../../public/Imgaes/service6-2x.jpg',
                        titolo: 'Crossfit workout',
                        didascalia: 'Push your limits'
                    },
                    {
                        imgUrl: '../../../public/Imgaes/box1-2x.jpg',
                        titolo: 'New gym apparel',
                        didascalia: 'Look good, feel good'
                    },
                    {
                        imgUrl: '../../../public/Imgaes/box3-2x.jpg',
                        titolo: 'Team training',
                        didascalia: 'Find a partner'
                    },
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section id="sezione-card">
            <div v-for="(element, index) in cards" :key="index">
                <figure>
                    <img :src="element.imgUrl" alt="">
                    <div id="didascalia-figure">
                        <h1>{{ element.titolo }}</h1>
                        <h3>{{ element.didascalia }}</h3>
                    </div>
                </figure>
            </div>    
        </section>
        <section id="sezione-scritta">
            <h1>“How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser.”</h1>
            <div>
                <img src="../../../public/Imgaes/avatar-1-2x.jpg" alt="">
                <h3>Brad Johnson</h3>
                <h4>Las Vegas</h4>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background: rgb(131,58,180);
        background: linear-gradient(117deg, rgba(11,21,209,1) 0%, rgba(88,11,117,1) 30%, rgba(185,4,44,1) 98%);
        height: 100vh; 
    }

    #sezione-card{
        @include page-layout;
        display: flex;
        gap: 35%;
        position: relative;    

        figure{
            position: absolute;
            top: -70px;

            img{
                width: 420px;
                image-rendering: crisp-edges;
                border-radius: 0 0 60px 0;
            }

            img:hover{
                    transform: scale(1.04);
                    transition: transform .35s;
            }

            #didascalia-figure{
                position: absolute;
                bottom: 50px;
                left: 50px;

                h1{
                    color: white;
                    font-weight: 600;
                }

                h3{
                    color: yellow;
                    font-weight: 600;
                }
            }
        }

        
    }
    #sezione-scritta{
        @include page-layout;
        h1{
            color: white;
            font-size: 40px;
            padding-top: 500px;
            width: 75%;
            margin: 0 auto;
            text-align: center;
        }

        div{
            img{
                width: 55px;
                border-radius: 100px;
            }

            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 60px;
            gap: 15px;

            h3{
                color: white;
            }

            h4{
                color: gray;
            }
        }
    }
</style>
