
<script>
    export default {
        name: "Section3"
    }
</script>






<template>
  
    <div id="section3Bg" class="py-5">
        <img src="../../assets/img/dog-left.png" alt="dog-img" id="dogLeftLogo">
        <img src="../../assets/img/dog-logo.png" alt="dog-img" id="dogRLogo">
        <div class="containerCustom m-auto text-center">
            <h5>Service</h5>
            <h2 class="m-auto">DogMilo Pet Care Services For Your Best Friends.</h2>
            <div class="d-flex gap-5 pt-5">
                <!--Card 1-->
                <div class="dogCard">
                    <img src="../../assets/img/d-1.png" alt="pet-sitting">
                    <h5>Pet Sitting</h5>
                    <p>
                        The readable content
                        of a page when
                        looking at its layout.
                    </p>
                    <a href="#" class="cardButton">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>
                </div>

                <!--Card 2-->
                <div class="dogCard">
                    <img src="../../assets/img/d-2.png" alt="pet-sitting">
                    <h5>Puppy Sitting</h5>
                    <p>
                        The readable content
                        of a page when
                        looking at its layout.
                    </p>
                    <a href="#" class="cardButton">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>
                </div>

                <!--Card 3-->
                <div class="dogCard">
                    <img src="../../assets/img/d-3.png" alt="pet-sitting">
                    <h5>Dog Walking</h5>
                    <p>
                        The readable content
                        of a page when
                        looking at its layout.
                    </p>
                    <a href="#" class="cardButton">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>
                </div>

                <!--Card 4-->
                <div class="dogCard">
                    <img src="../../assets/img/d-4.png" alt="pet-sitting">
                    <h5>Night Care</h5>
                    <p>
                        The readable content
                        of a page when
                        looking at its layout.
                    </p>
                    <a href="#" class="cardButton">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>
                </div>

                <!--Card 4-->
                <div class="dogCard">
                    <img src="../../assets/img/d-5.png" alt="pet-sitting">
                    <h5>Pet Sitting</h5>
                    <p>
                        The readable content
                        of a page when
                        looking at its layout.
                    </p>
                    <a href="#" class="cardButton">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </div>



</template>








<style lang="scss" scoped>
    @import '../../scss/styles.scss';
    #section3Bg{
        position: relative;
        background-color: #f5f5f5;
        #dogLeftLogo{
            position: absolute;
            width: 10%;
        }
        #dogRLogo{
            position: absolute;
            right: 0;
            width: 12%;
        }
        h2{
            width: 45%;
        }
        .dogCard{
            display: flex;
            flex-direction: column;
            --gap: 3rem;
    		--columns: 5;
    		flex-basis: calc((100% / var(--columns)) - var(--gap) + (var(--gap) / var(--columns)));
            align-items: center;
            justify-content: center;
            background-color: $primaryColor;
            border-radius: 100px;
            padding: 1rem;
            gap: 0.8rem;
            color: white;
            &:hover{
                background-color: #7f7045;
            }
            img{
                width: 40%;
                margin-bottom: 1rem;
            }
            svg{
                width: 30%;
                background-color: #ffcc00;
                border-radius: 100px;
                padding-block: 15px;
                padding-inline: 20px;
            }
        }
    }




</style>