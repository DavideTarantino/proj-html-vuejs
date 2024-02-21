<script>
    export default {
        name: 'SectionSeven',
        data(){
            return{}
        }
    }
</script>

<template>
    <main>
        <div>
            <h1>“I've failed over and over again in my life. And that is why I succeed.”</h1>
            <p>Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed massa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis</p>
            <button>Buy Avada Today ></button>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background-blend-mode: multiply;
        background-image: linear-gradient(0deg, black 1%,white 100%), url(../../../public/Imgaes/banner2-2x.jpg);
        //background-image: url(../../../public/Imgaes/banner2-2x.jpg);
        height: 80vh;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;

        div{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding-top: 10%;

            h1{
                width: 55%;
                color: white;
                font-size: 60px;
                text-align: center;
            }

            p{
                color: white;
                margin-top: 5%;
                width: 55%;
                text-align: center;
                font-size: 25px;
                font-weight: 300;
            }

            button{
                margin-top: 3%;
                padding-block: 1%;
                padding-inline: 3%;
                background-color: #4154FF;
                color: white;
                border-radius: 50px;
                border: none;
                font-size: 18px;
                cursor: pointer;
            }

            button:hover{
                background-color: #FF414B;
            }
        }
    }
</style>