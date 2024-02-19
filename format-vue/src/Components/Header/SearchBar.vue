<script>
    export default {
        name: 'SearchBar',
        data(){
            return{
                Links: [
                    {
                        name: 'Home',
                        news: 'false'
                    },
                    {
                        name: 'Services',
                        news: 'false'
                    },
                    {
                        name: 'About',
                        news: 'false'
                    },
                    {
                        name: 'Videos',
                        news: 'false'
                    },
                    {
                        name: 'Blog',
                        news: 'false'
                    },
                    {
                        name: 'Store',
                        news: 'true'
                    } 
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section>
            <div>
                <img src="../../../public/Imgaes/logo-200x34.png" alt="">
            </div>
            <div>
                <div id="container-links">
                    <ul v-for="(element, index) in Links" :key="index">
                        <li>
                            {{ element.name }}
                            <span :class="(element.news === 'true') ? 'active' : ''">new</span>
                        </li>
                    </ul>
                    <button>Scedule a workout</button>
                    <i class="fa-solid fa-cart-shopping" style="color: #c7cdd6;"></i>
                    <i class="fa-solid fa-magnifying-glass" style="color: #c0c7d3;"></i>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../../Styles/partials/mixins' as*;

    main{
        background-color: black;
        padding-block: 2%;
        
        section{
            @include page-layout;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        #container-links{
            display: flex;
            gap: 20px;
            align-items: center;
        
            ul{
                li{
                    color: gray;
                    list-style-type: none;
                    cursor: pointer;
                    display: flex;
                    gap: 5px;
                    align-items: center;
    
                    span{
                        background-color: yellow;
                        padding: 2px;
                        color: black;
                        border-radius: 3px;
                        display: none;
                    }
                    
                    .active{
                        display: block;
                    }
                }
    
                li:hover{
                    color: white;
                }
            }

            button{
                background-color: #4154FF;
                color: white;
                padding-block: 12px;
                padding-inline: 22px;
                border-radius: 20px;
                border: none;
                cursor: pointer;
            }

            button:hover{
                background-color: lightblue;
            }
        }

    }
</style>
