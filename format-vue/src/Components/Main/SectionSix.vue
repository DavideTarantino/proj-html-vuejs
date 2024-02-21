<script>
    export default {
        name: 'SectionSix',
        data(){
            return{
                cards: [
                    {
                        imgUrl: '../../../Imgaes/blog4-2x-600x386.jpg',
                        title: 'The best protein shake',
                        description: 'Published On: November 26th, 2019 | 2 Comments'
                    },
                    {
                        imgUrl: '../../../Imgaes/blog1-2x-1200x773.jpg',
                        title: 'Ultimate cardio workout',
                        description: 'Published On: November 26th, 2019 | 0 Comments'
                    },
                    {
                        imgUrl: '../../../Imgaes/blog3-2x-1200x773.jpg',
                        title: 'New juices available now',
                        description: 'Published On: November 26th, 2019 | 0 Comments'
                    }
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section>
            <div id="head">
                <h1>
                    Latest articles
                </h1>
                <h4>
                    Read all articles >
                </h4>
            </div>
            <div id="body-section">
                <div id="body" v-for="(element, index) in cards" :key="index">
                    <img :src="element.imgUrl" alt="">
                    <h1>{{ element.title }}</h1>
                    <p>{{ element.description }}</p>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        height: 60vh;

        section{
            @include page-layout;

            #head{
                padding-top: 8%;
                display: flex;
                justify-content: space-between;
            }
        }

        #body-section{
            margin-top: 30px;
            display: flex;
            justify-content: space-between;

            #body{
                img{
                    width: 400px;
                    margin-bottom: 25px;
                }
                h1{
                    font-weight: 400;
                    margin-bottom: 17px;
                }
                p{
                    font-weight: 300;
                }
            }
        }
    }
</style>