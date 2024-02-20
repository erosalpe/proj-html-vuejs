
<script>
    export default {
        name: "Section1"
    }
</script>






<template>
    <div id="section1Bg">
        <div id="infoBlock1" class="containerCustom m-auto d-flex flex-column justify-content-center text-light h-100 gap-4">
            <h1>
                Welcome to <span>DogMilo</span> Pets
            </h1>
            <span>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dummy text placeholder.
            </span>
            <div class="d-flex gap-3 justify-content-start align-items-center">
                <a href="#" class="primaryButton">
                    <span>
                        get in touch!
                    </span>
                </a>
                <a href="#" class="socialButton">
                    <img src="../../assets/img/play.png" alt="playback">
                </a>
            </div>
        </div>
    </div>
  

  


</template>








<style lang="scss" scoped>
     @import '../../scss/styles.scss';

     #section1Bg{
        background-image: url(../../assets/img/b.png);
        height: 600px;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: 10%;
        #infoBlock1{
            h1{
                width: 35%;
                font-size: 50px;
                span{
                    font-weight: 400;
                }
            }
            >span{
                width: 40%;
                font-weight: 500;
            }
        }
     }
     .socialButton{
        background-color: #71d0f7;
        padding: 5px;
        border-radius: 10px;
        img{
            width:40px;
        }
     }




</style>