<script>
    export default {
        name: 'SectionThree',
        data(){
            return{
                videos: [
                    {
                        imgUrl: '../../../public/Imgaes/video2-2x.jpg',
                        title: 'Tighs & glute workout',
                        description: 'Increase your mobility'
                    },
                    {
                        imgUrl: '../../../public/Imgaes/video7-2x.jpg',
                        title: 'Lift, firm & perk up',
                        description: 'Fell young again'
                    },
                    {
                        imgUrl: '../../../public/Imgaes/video9-2x.jpg',
                        title: 'Slim & trim your waist',
                        description: 'Shed those extra pounds'
                    },
                ]
            }
        }
    }
</script>

<template>
<main>
    <section id="sezione-video-grande">
        <div id="miniatura-video">
            <img src="../../../public/Imgaes/service15-2x.jpg" alt="">
            <a href="#"><i class="fa-solid fa-play"></i></a>
        </div>
        <div id="didascalia-video">
            <h2>Tune up your workouts</h2>
            <h1>The best health & fitness advice online</h1>
            <p>Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer sit pellentesque.</p>
            <button id="button-1"><i class="fa-brands fa-youtube" style="color: #ffffff;"></i> Visit my YouTube channel</button>
        </div>
    </section>
    <section id="sezione-consigliati">
        <div id="head">
            <h1>Featured playlists</h1>
            <a href="#">View all videos  ></a>
        </div>
        <div id="body">
            <div v-for="(element, index) in videos" :key="index">
                <img :src="element.imgUrl" alt="">
                <h3>{{ element.title }}</h3>
                <p>{{ element.description }}</p>
                <a href="#"><i class="fa-solid fa-play"></i></a>
            </div>
        </div>
    </section>
</main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    #sezione-video-grande{
        position: relative;
        height: 820px;

        #miniatura-video{
            position: absolute;
            top: -70px;
            
            img{
                width: 850px;
                height: 800px;
                border-radius: 0 0 60px 0;
            }

            a{
                position: absolute;
                top: 50%;
                left: 50%;
                background-color: white;
                padding: 30px;
                border-radius: 50px;
                margin-left: -35px;
                margin-top: -35px;
                color: blue;
            }

            a:hover{
                color: orangered;
            }
        }

        #didascalia-video{
            margin-left: 1000px;
            padding-top: 150px;

            h2{
                color: blue;
                font-size: 30px;
                margin-bottom: 50px;
            }

            h1{
                font-size: 60px;
                width: 80%;
                margin-bottom: 30px;
            }

            p{
                font-size: 20px;
                font-weight: 400;
                width: 82%;
                color: gray;
                margin-bottom: 30px;
            }

            #button-1{           
            padding-block: 2%;
            padding-inline: 5%;
            border-radius: 25px;
            color: white;
            font-size: 15px;
            border: none;
            background-color: red;
            cursor: pointer;
            }
        }
    }

    #sezione-consigliati{
        @include page-layout;

        img{
            width: 400px;
            border-radius: 5px 5px 60px 5px;
            margin-bottom: 25px;
        }

        #head{
            display: flex;
            justify-content: space-between;
            align-items: center;

            a{
                text-decoration: none;
                color: black;
            }

            a:hover{
                color: blue;
            }
        }

        #body{
            display: flex;
            gap: 5%;
            margin-top: 25px;
            position: relative;

            div{
                display: flex;
                flex-direction: column;
                align-items: center;

                p{
                    color: blue;
                }

                a{
                    position: absolute;
                    top: 100px;
                    background-color: white;
                    padding: 1%;
                    border-radius: 50px;
                }
            }
        }
    }
</style>