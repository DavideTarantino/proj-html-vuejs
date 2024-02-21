<script>
    export default {
        name: 'SectionFour',
        data(){
            return{}
        }
    }
</script>

<template>
    <main>
        <section>
            <h3>Join our mailing list today</h3>
            <h1>Insider offers & flash sales in your inbox every week.</h1>
            <div>
                <input type="text" placeholder="Insert your email...*">
                <button>Subscribe</button>
            </div>
            <p>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur adipiscing elit sed porttitor lectus.</p>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background-blend-mode: multiply;
        background-image: linear-gradient(90deg, black 35%,white 100%), url(../../../public/Imgaes/banner1-2x.jpg);
        //background-image: url(../../../public/Imgaes/banner1-2x.jpg);
        height: 80vh;
        background-size: cover;
        background-position: right;
        background-repeat: no-repeat;

        section{
        @include page-layout;

            h3{
                padding-top: 7%;
                color: #FF414B;
                font-size: 25px;
            }

            h1{
                margin-top: 2%;
                color: white;
                font-size: 50px;
                width: 60%;
            }

            div{
                margin-top: 5%;
                display: flex;
                gap: 3%;

                input{
                    padding-block: 20px;
                    padding-left: 1%;
                    padding-right: 32%;
                    border-radius: 30px;
                    border: none;
                }

                input::placeholder{
                    color: gray;
                    font-size: 15px;
                }

                button{
                    background-color: #4154FF;
                    padding-inline: 7%;
                    border-radius: 30px;
                    border: none;
                    color: white;
                    font-size: 17px;
                    cursor: pointer;
                }

                button:hover{
                    background-color: #FF414B;
                }
                
            }
                p{
                    color: whitesmoke;
                    margin-top: 7%;
                    font-size: 20px;
                    font-weight: 300;
                    width: 65%;
                }
        }
    }
</style>