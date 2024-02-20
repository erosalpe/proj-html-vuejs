
<script>
    export default {
        name: "Section5"
    }
</script>






<template>
    <div class="container containerCustom m-auto pt-5">
        <div class="row">
            <div class="col-4">
                <div class="d-flex align-items-center gap-3 pawTitle pb-4">
                    <img src="../../assets/img/dog-icon.png" alt="dog-paw" class="pawImage">
                    <span class="fs-7">Review & Rating</span>
                 </div>
                <h2 class="fs-3">
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
                    <div class="caroselloCard d-flex flex-column p-3 gap-3">
                        <span class="d-block">
                            &#11088;&#11088;&#11088;&#11088;&#11088;
                        </span>
                        <h4>Great Place</h4>
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

                    <div class="caroselloCard d-flex flex-column p-3 gap-3">
                        <span class="d-block">
                            &#11088;&#11088;&#11088;&#11088;&#11088;
                        </span>
                        <h4>Great Place</h4>
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
    #carosello{
        background-color: black;
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
</style>