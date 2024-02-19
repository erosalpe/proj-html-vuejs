
<script>
    export default {
        name: "Section4"
    }
</script>






<template>
  
    <div class="d-flex">
        <img src="../../assets/img/why.png" alt="why-img" class="w-50">
        <div class="d-flex flex-column pt-5 ps-5 gap-2">
            <div class="d-flex align-items-center gap-3 pawTitle">
                <img src="../../assets/img/dog-icon.png" alt="dog-paw" class="pawImage">
                <span class="fs-7">Choose Us</span>
            </div>
            <div class="whyUsP">
                <h2 class="mb-4">Why choose Us?</h2>
                <div class="d-flex gap-5 w-75">
                    <img src="../../assets/img/w-3.png" alt="why-us" class="whyUsImg"> 
                    <div class="d-flex flex-column gap-3">
                        <h4>Safety First</h4>
                        <p> 
                            It is a long established fact that a reader will be distructed by the readable content of a
                            page when looking at its layout.
                        </p>
                    </div>
                </div>
            </div>

            <div class="whyUsP">
                <div class="d-flex gap-5 w-75">
                    <img src="../../assets/img/w-2.png" alt="why-us" class="whyUsImg"> 
                    <div class="d-flex flex-column gap-3">
                        <h4>Play Yards</h4>
                        <p> 
                            It is a long established fact that a reader will be distructed by the readable content of a
                            page when looking at its layout.
                        </p>
                    </div>
                </div>
            </div>

            <div class="whyUsP">
                <div class="d-flex gap-5 w-75">
                    <img src="../../assets/img/w-1.png" alt="why-us" class="whyUsImg"> 
                    <div class="d-flex flex-column gap-3">
                        <h4>Monitor Your Pets</h4>
                        <p> 
                            It is a long established fact that a reader will be distructed by the readable content of a
                            page when looking at its layout.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>

  


</template>








<style lang="scss" scoped>
    
    .pawTitle{
        span{
            color: #887D62;
            font-weight: bold;
        }
    }
    .pawImage{
        width: 7%;
    }
    .whyUsImg{
        width: 20%;
    }

    .whyUsP{
        &:nth-child(3){
            padding-left: 200px;
        }
        &:nth-child(4){
            padding-left: 400px;
            .whyUsImg{
                width: 25%;
            }
        }
    }



</style>