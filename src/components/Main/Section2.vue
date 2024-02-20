
<script>
    export default {
        name: "Section2"
    }
</script>






<template>
    <div id="section2Bg" class="position-relative">
        <div class="containerCustom m-auto d-flex gap-5 py-5">
            <img src="../../assets/img/about.png" alt="about-img" id="aboutImg">
            <div>
                <div class="d-flex flex-column justify-content-center h-100 gap-3">
                    <div class="d-flex align-items-center gap-3">
                        <img src="../../assets/img/dog-icon.png" alt="dog-paw">
                        <span class="fs-7">About Us</span>
                    </div>
                    <h2 class="fs-1">
                        Welcome DogMilo Pets
                    </h2>
                    <p>
                        Lorem Ipsum is simply dummy text of the printing and typesetting
                        industry. Lorem Ipsum has been the industry's standard dummy text
                        ever since the 1500s, when an unknown printer took a galley of type
                        and scrambled.
                    </p>
                    <p>
                        Lorem Ipsum is simply dummy text of the printing and typesetting
                        industry. Lorem Ipsum has been the industry's standard dummy text
                        ever since the 1500s, when an unknown printer took a galley of type
                        and scrambled
                    </p>
                </div>
            </div>
        </div>
        <img src="../../assets/img/dog-logo.png" alt="dog.logo" class="position-absolute">
    </div>
  



</template>








<style lang="scss" scoped>
    @import '../../scss/styles.scss';
    #section2Bg>img{
        top: 3rem;
        right: 0;
    }

    #aboutImg{
        width: 45%;
    }
    .d-flex.align-items-center.gap-3{
        span{
            color: #887D62;
            font-weight: bold;
        }
    }

    
</style>