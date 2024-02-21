
<script>
    export default {
        name: "Section5",
        data(){
            return{
                reviewArray: [
                    {   
                        id: 0,
                        stars: 1,
                        title: 'Great Place',
                        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry s standard dummy text ever since the 1500s, when',
                        profilePic: './src/assets/img/t1.png',
                        name: 'Tobias May',
                        job: 'UI/UX Designer',
                        active: true,
                    },
                    {
                        id: 1,
                        stars: 2,
                        title: 'Great Place',
                        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry s standard dummy text ever since the 1500s, when',
                        profilePic: './src/assets/img/t1.png',
                        name: 'Tobias May',
                        job: 'UI/UX Designer',
                        active: true,
                    },
                    {
                        id: 2,
                        stars: 3,
                        title: 'Great Place',
                        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry s standard dummy text ever since the 1500s, when',
                        profilePic: './src/assets/img/t1.png',
                        name: 'Tobias May',
                        job: 'UI/UX Designer',
                        active: false,
                    },
                    {
                        id: 3,
                        stars: 4,
                        title: 'Great Place',
                        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry s standard dummy text ever since the 1500s, when',
                        profilePic: './src/assets/img/t1.png',
                        name: 'Tobias May',
                        job: 'UI/UX Designer',
                        active: false,
                    },
                    {
                        id: 3,
                        stars: 5,
                        title: 'Great Place',
                        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry s standard dummy text ever since the 1500s, when',
                        profilePic: './src/assets/img/t1.png',
                        name: 'Tobias May',
                        job: 'UI/UX Designer',
                        active: false,
                    },
                ],
                firstId: 0,
                secondId: 1,
            }
           
        },
        methods:{
            nextRev(){
                if(this.secondId > this.reviewArray.length -2){
                    this.reviewArray.forEach(element => {
                        element.active = false
                    });
                    this.firstId = 0
                    this.secondId = 1
                    this.reviewArray[this.firstId].active = true
                    this.reviewArray[this.secondId].active = true
                } else {
                    this.reviewArray[this.firstId].active = false
                    this.firstId++;
                    this.secondId++;
                    this.reviewArray[this.secondId].active = true
                }
            },
            prevRev(){
                if(this.firstId === 0){
                    this.reviewArray.forEach(element => {
                        element.active = false
                    });
                    this.firstId = this.reviewArray.length - 2
                    this.secondId = this.reviewArray.length - 1
                    this.reviewArray[this.firstId].active = true
                    this.reviewArray[this.secondId].active = true
                } else {
                    this.reviewArray[this.secondId].active = false
                    this.reviewArray[this.firstId].active = false
                    this.secondId--;
                    this.firstId--;
                    this.reviewArray[this.secondId].active = true
                    this.reviewArray[this.firstId].active = true
                }
            }
        }
    }
</script>






<template>
    <div class="container containerCustom m-auto pt-5" id="reviewBody">
        <div class="row">
            <div class="col-4">
                <div class="d-flex align-items-center gap-3 pawTitle">
                    <img src="../../assets/img/dog-icon.png" alt="dog-paw" class="pawImage">
                    <span class="fs-7">Review & Rating</span>
                 </div>
                <h2 class="fs-3 py-4 w-75">
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
                <div class="w-100 h-100 d-flex gap-4 overflow-hidden" id="carosello">
                    <div class="caroselloCard d-flex flex-column p-3" v-for="element in reviewArray" :class="{'d-none' : !element.active}">
                        <span class="d-block">
                            <span v-for="index in element.stars">
                                &#11088;
                            </span>
                        </span>
                        <h4 class="py-2">{{ element.title }}</h4>
                        <p>
                            {{ element.description}}
                        </p>
                        <div class="d-flex align-items-end gap-2 h-100">
                            <div class="d-flex align-items-center gap-2">
                                <img :src="element.profilePic" alt="profile-pic">
                                <div class="d-flex flex-column gap-3">
                                    <span class="fw-bold">
                                        {{ element.name }}
                                    </span>
                                    <span class="revJob">
                                        {{ element.job }}
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex gap-3 justify-content-end pt-3">
                    <svg @click="prevRev()" id="arrowL" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path fill="#FFFFFF" d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg>
                
                    <svg @click="nextRev()" id="arrowR" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path fill="#FFFFFF" d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>
                </div>
            </div>
        </div>
    </div>
  


  


</template>








<style lang="scss" scoped>
    @import '../../scss/styles.scss';
    #reviewBody{
        padding-bottom: 100px;
    }
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

    .active{
        display: block;
    }
</style>