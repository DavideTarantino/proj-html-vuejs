<script>
    export default {
        name: 'SectionOne',
        data(){
            return{currentImage: 0,
            autoScroll: null,
            slides: [
                    {
                        image: '../../../public/Imgaes/slider82x-scaled.jpg',
                        redTitle: 'Certified fitness professional',
                        title: 'Take Control of your healt',
                        text: 'Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.',
                        slide: 'true'
                    }, 
                    {
                        image: '../../../public/Imgaes/banner2-2x.jpg',
                        title: 'Watch my latest videos',
                        text: 'Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur adipiscing elit sed porttitor lectus.',
                        slide: 'false'
                    }, 
                ],
            }
        },
      methods: {
        nextImage(){
          this.currentImage++
    
          if( this.currentImage > this.slides.length - 1  ){
            this.currentImage = 0
          }
        },
         changeImage(index){
           this.currentImage = index
         }
      }
    }
</script>

<template>
    <main>
        <div class="container">
            <div class="slider-wrapper" tabindex="0">

                <div class="item">
                    <img :src="slides[currentImage].image" alt="Spiderman" />
                    <div class="text"> 
                        <h2>{{ slides[currentImage].redTitle }}</h2>  
                        <h1>{{ slides[currentImage].title }}</h1>
                        <p>
                            {{ slides[currentImage].text }}
                        </p>
                        <div id="button-container">
                            <button id="button-1"><i class="fa-brands fa-youtube" style="color: #ffffff;"></i> Visit my YouTube channel</button>
                            <button id="button-2">Buy Avada today <i class="fa-solid fa-arrow-right-long"></i></button>
                        </div>
                    </div>
                    <div class="next" @click="nextImage"><i class="fa-solid fa-play" style="color: #075ae9;"></i></div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
.item {
    float: left;
    width: 100%;
    height: 650px;
    position: relative;

    
    #button-container{
        display: flex;
        gap: 20px;

        #button-1, #button-2{           
            padding: 2%;
            border-radius: 25px;
            color: white;
            font-size: 15px;
        }

        #button-1{
            border: none;
            background-color: #4154FF;
            cursor: pointer;
        }

        #button-1:hover{
            background-color: #EF414B;
        }

        #button-2{
            background-color: black;
            border: 2px solid gray;
        }

        #button-2:hover{
            background-color: white;
            color: black;
        }
    }
}

.item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
}

.item .text {
    position: absolute;
    left: 280px;
    bottom: 300px;
    text-align: left;
    color: white;
    line-height: 80px;

    h2{
        color: red;
    }

    h1{
        font-size: 70px;
    }
}

.next {
    padding-block: 2%;
    padding-inline: 40px;
    margin: 10px 0;
    bottom: 300px;
    border-radius: 50%;
    background: white;
    position: absolute;
    cursor: pointer;
    z-index: 999;
    right: 380px;
    font-size: 20px;
}
</style>
