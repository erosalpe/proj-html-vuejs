
<script>
    export default {
        name: "Section5"
    }
</script>






<template>
    <div class="container containerCustom m-auto pt-5">
        <div class="row">
            <div class="col-4">
                <div class="d-flex align-items-center gap-3 pawTitle">
                    <img src="../../assets/img/dog-icon.png" alt="dog-paw" class="pawImage">
                    <span class="fs-7">Review & Rating</span>
                 </div>
                <h2 class="fs-3 py-4">
                    Over 8000 Customers With 5-Star Review
                </h2>
                <p>
                    It is a long established fact that a reader will be
                    distructed by the readable content of a page when
                    looking at its layout.
                </p>
                <span class="d-block pt-3">
                    &#11088;&#11088;&#11088;&#11088;&#11088;
                </span>
            </div>
            <div class="col-8">
                <div class="w-100 h-100 d-flex gap-4" id="carosello">
                    <div class="caroselloCard d-flex flex-column p-3">
                        <span class="d-block">
                            &#11088;&#11088;&#11088;&#11088;&#11088;
                        </span>
                        <h4 class="py-2">Great Place</h4>
                        <p>
                            Lorem Ipsum is simply dummy text of the
                            printing and typesetting industry. Lorem
                            Ipsum has been the industry's standard
                            dummy text ever since the 1500s, when
                        </p>
                        <div class="d-flex align-items-end gap-2 h-100">
                            <div class="d-flex align-items-center gap-2">
                                <img src="../../assets/img/t1.png" alt="profile-pic">
                                <div class="d-flex flex-column gap-3">
                                    <span class="fw-bold">
                                        Tobias May
                                    </span>
                                    <span class="revJob">
                                        UI/UX Designer
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="caroselloCard d-flex flex-column p-3">
                        <span class="d-block">
                            &#11088;&#11088;&#11088;&#11088;&#11088;
                        </span>
                        <h4 class="py-2">Great Place</h4>
                        <p>
                            Lorem Ipsum is simply dummy text of the
                            printing and typesetting industry. Lorem
                            Ipsum has been the industry's standard
                            dummy text ever since the 1500s, when
                        </p>
                        <div class="d-flex align-items-end gap-2 h-100">
                            <div class="d-flex align-items-center gap-2">
                                <img src="../../assets/img/t1.png" alt="profile-pic">
                                <div class="d-flex flex-column gap-3">
                                    <span class="fw-bold">
                                        Tobias May
                                    </span>
                                    <span class="revJob">
                                        UI/UX Designer
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex gap-3 justify-content-end pt-3">
                    <svg id="arrowL" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path fill="#FFFFFF" d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg>
                
                    <svg id="arrowR" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path fill="#FFFFFF" d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>
                </div>
            </div>
        </div>
    </div>
  


  


</template>








<style lang="scss" scoped>
    @import '../../scss/styles.scss';
    .pawTitle{
        img{
            width: 9%;
        }
        span{
            color: #887D62;
            font-weight: bold;
        }
    }
    .caroselloCard{
        --gap: 1.5rem;
        --columns: 2;
        flex-basis: calc((100% / var(--columns)) - var(--gap) + (var(--gap) / var(--columns)));
        background-color: #f4f4f4;
        img{
            width: 20%;
            border-radius: 50px;
        }
        .revJob{
            font-size: 13px;
        }
    }
    #arrowL,
    #arrowR{
        background-color: $primaryColor;
        padding-inline: 8px;
        padding-block: 2px;
        width: 35px;
        &:hover{
            background-color: #7f7045;
        }
    }
</style>