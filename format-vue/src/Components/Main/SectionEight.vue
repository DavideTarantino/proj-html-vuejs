<script>
    export default {
        name: 'SectionEight',
        data(){
            return{
                cards:[
                    {
                        imgUrl: '../../../Imgaes/sponsor-1-2x-200x103.png',
                        description: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                        link: 'Visit Yoga Studio >'
                    },
                    {
                        imgUrl: '../../../Imgaes/sponsor-2-2x-200x103.png',
                        description: 'Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.',
                        link: 'Join Fitness Center >'
                    },
                    {
                        imgUrl: '../../../Imgaes/sponsor-3-2x-200x103.png',
                        description: 'Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et sagittis imperdiet.',
                        link: 'Learn about FC >'
                    },
                    {
                        imgUrl: '../../../Imgaes/sponsor-4-2x-200x103.png',
                        description: 'Proin in viverra maecenas et mattis ut nibh enim. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.',
                        link: 'Visit Power Gym >'
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
                <img :src="element.imgUrl" alt="">
                <p>{{ element.description }}</p>
                <h3>{{ element.link }}</h3>
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
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 8%;
            padding-top: 7%;

            div{
                display: flex;
                flex-direction: column;
                align-items: center;

                p{
                    margin-top: 12%;
                    text-align: center;
                    font-size: 18px;
                    font-weight: 300;
                }
                h3{
                    text-align: center;
                    margin-top: 15%;
                }
            }
        }
    }
</style>