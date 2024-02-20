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
        <section>
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
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background: rgb(131,58,180);
        background: linear-gradient(117deg, rgba(11,21,209,1) 0%, rgba(88,11,117,1) 30%, rgba(185,4,44,1) 98%);
    }

    section{
        @include page-layout;
        display: flex;
        gap: 35%;
        position: relative;
        height: 100vh;    

        figure{
            position: absolute;
            top: -70px;

            img{
                width: 420px;
                image-rendering: crisp-edges;
                border-radius: 0 0 60px 0;
            }

            img:hover{
                width: 430px;
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
</style>
