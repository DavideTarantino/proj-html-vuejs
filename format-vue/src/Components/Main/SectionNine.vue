<script>
    export default {
        name: 'SectionNine',
        data(){
            return{}
        }
    }
</script>

<template>
    <main>
        <div>
            <a href="#"><i class="fa-solid fa-play"></i></a>
            <h1>Crossfit workout of the day</h1>
            <h2>November 15th, 2019</h2>
            <p>View all videos <i class="fa-solid fa-arrow-right"></i></p>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background-blend-mode: multiply;
        background-image: linear-gradient(151deg, blue 35%,red 100%), url(../../../public/Imgaes/banner14-2x.jpg);
        height: 73vh;
        background-size: contain;

        div{
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding-top: 10%;
            
            a{
                background-color: white;
                padding: 2%;
                border-radius: 50px;
                margin-bottom: 35px;
            }

            h1{
                font-size: 50px;
                font-weight: 400;
            }

            h2{
                color: yellow;
                font-size: 35px;
                margin-top: 20px;
            }

            p{
                margin-top: 20px;
                font-size: 20px;
                font-weight: 300;
                cursor: pointer;
            }
        }
    }
</style>