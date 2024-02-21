<script>
    export default {
        name: 'SectionFive',
        data(){
            return{
                cards:[
                    {
                        title: 'Team Training',
                        yellowTitle: 'Find a partner',
                        description: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
                        link: 'Find a partner >'
                    },
                    {
                        title: 'Crossfit workout',
                        yellowTitle: 'Push your limits',
                        description: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
                        link: 'Learn about crossfit >'
                    },
                    {
                        title: 'Weight loss plan',
                        yellowTitle: 'Shed those pounds',
                        description: 'At laoreet senectus volutpat diam vel sed sed amet pellentesque. Lobortis ut aliquam risus purus. A tellus ut etiam.',
                        link: 'Schedule a workout >'
                    },
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section>
            <div>
                <p class="icons"><i class="fa-solid fa-stopwatch-20"></i></p>
                <h1>{{ cards[0].title }}</h1>
                <h2>{{ cards[0].yellowTitle }}</h2>
                <p class="description">{{ cards[0].description }}</p>
                <p class="links">{{ cards[0].link }}</p>
            </div>
            <div>
                <p class="icons"><i class="fa-solid fa-dumbbell"></i></p>
                <h1>{{ cards[1].title }}</h1>
                <h2>{{ cards[1].yellowTitle }}</h2>
                <p class="description">{{ cards[1].description }}</p>
                <p class="links">{{ cards[1].link }}</p>
            </div>
            <div>
                <p class="icons"><i class="fa-solid fa-weight-scale"></i></p>
                <h1>{{ cards[2].title }}</h1>
                <h2>{{ cards[2].yellowTitle }}</h2>
                <p class="description">{{ cards[2].description }}</p>
                <p class="links">{{ cards[2].link }}</p>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

main{
    height: 80vh;
    background-color: black;
    color: white;

    section{
        @include page-layout;
        padding-top: 6%;
        display: flex;
        justify-content: space-between;

        div{
            width: 30%;
            display: flex;
            flex-direction: column;
            align-items: center;
            border: 4px solid #4154FF;
            border-radius: 10px;
            padding: 2%;
            cursor: pointer;

            .icons{
                font-size: 70px;
                margin-bottom: 20px;
                margin-top: 40px;
            }

            h2{
                color: yellow;
                margin-bottom: 40px;
            }

            .description{
                text-align: center;
                font-weight: 300;
                line-height: 23px;
                font-size: 17px;
                width: 80%;
                margin-bottom: 40px;
            }

            .links{
                margin-bottom: 60px;
            }
        }
        div:hover{
            transform: scale(1.04);
            transition: transform .35s;
        }
    }
}
</style>