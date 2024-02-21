
<script>
    import Socials from './Header/Socials.vue'
    import { store } from '../store'
    export default {
        name: "FooterComponent",
        components:{
            Socials
        },
        data(){
            return{
                supportArray:[
                    {
                        name: 'contact us',
                        link: '#'
                    },
                    {
                        name: 'online chat',
                        link: '#'
                    },
                    {
                        name: 'whatsapp',
                        link: '#'
                    },
                    {
                        name: 'telegram',
                        link: '#'
                    },
                    {
                        name: 'snapchat',
                        link: '#'
                    },
                ],
                aboutArray:[
                    {
                        name: 'about us',
                        link: '#'
                    },
                    {
                        name: 'blog chat',
                        link: '#'
                    },
                    {
                        name: 'career',
                        link: '#'
                    },
                    {
                        name: 'job',
                        link: '#'
                    },
                    {
                        name: 'in press',
                        link: '#'
                    },
                ],
                faqArray:[
                    {
                        name: 'account',
                        link: '#'
                    },
                    {
                        name: 'order',
                        link: '#'
                    },
                    {
                        name: 'delivery',
                        link: '#'
                    },
                    {
                        name: 'payment',
                        link: '#'
                    },
                    {
                        name: 'return',
                        link: '#'
                    },
                ],
                store,
            }
        },
        methods:{
            addEmail(mail){
                if(store.userEmail && store.userEmail.trim() && store.userEmail.includes('@')){
                    store.usersEmailsArray.push(mail)
                    store.userEmail = ''
                } else {
                    
                    store.emailPopup = true
                    console.log("email sbagliata", store.emailPopup)
                    setTimeout(()=>{
                        store.emailPopup = false
                    }, 5000)
                    console.log("email sbagliata", store.emailPopup)
                }
            }
        }
    }
</script>






<template>
  
    <div id="footerBg">


        <div id="floatingNews">
            <div class="d-flex w-50 m-auto" id="newsLetter">
                <img src="../assets/img/news.png" alt="news-img">
                <div class="d-flex justify-content-end w-100">
                    <div class="d-flex flex-column pe-4 py-0">
                        <h2 class="pb-2 text-light">
                            Subscribe to Our Newsletter
                        </h2>
                        <div class="p-0" id="emailField">
                            <input type="text" name="userEmail" id="newsletterEmail" placeholder="Your Email Here" class="w-100" v-model="store.userEmail" @keyup.enter="addEmail(store.userEmail)">
                            <a @click=" addEmail(store.userEmail)">
                                <span>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="40px" viewBox="0 0 512 512"><path fill="#ffffff" d="M256 64C150 64 64 150 64 256s86 192 192 192c17.7 0 32 14.3 32 32s-14.3 32-32 32C114.6 512 0 397.4 0 256S114.6 0 256 0S512 114.6 512 256v32c0 53-43 96-96 96c-29.3 0-55.6-13.2-73.2-33.9C320 371.1 289.5 384 256 384c-70.7 0-128-57.3-128-128s57.3-128 128-128c27.9 0 53.7 8.9 74.7 24.1c5.7-5 13.1-8.1 21.3-8.1c17.7 0 32 14.3 32 32v80 32c0 17.7 14.3 32 32 32s32-14.3 32-32V256c0-106-86-192-192-192zm64 192a64 64 0 1 0 -128 0 64 64 0 1 0 128 0z"/></svg>
                                </span>
                            </a>
                            <Transition>
                                <div class="p-1 m-0" id="emailPopup" v-if="store.emailPopup">
                                    <svg width="16px" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 630">
                                        <path fill="#ffbb00" d="M256 32c14.2 0 27.3 7.5 34.5 19.8l216 368c7.3 12.4 7.3 27.7 .2 40.1S486.3 480 472 480H40c-14.3 0-27.6-7.7-34.7-20.1s-7-27.8 .2-40.1l216-368C228.7 39.5 241.8 32 256 32zm0 128c-13.3 0-24 10.7-24 24V296c0 13.3 10.7 24 24 24s24-10.7 24-24V184c0-13.3-10.7-24-24-24zm32 224a32 32 0 1 0 -64 0 32 32 0 1 0 64 0z"/>
                                    </svg>
                                    L'indirizzo mail deve rispettare il seguente formato:<br>info@example.com
                                </div>
                            </Transition>
                        </div>
                    </div>
                </div>
            </div>
        </div>





        <div class="border-bottom pb-4" id="borderFooter">
            <div class="d-flex justify-content-between containerCustom m-auto">
                <div class="d-flex flex-column gap-2">
                    <h5 class="text-capitalize">get in touch</h5>
                    <a href="#">
                        <p>
                            Have a question for us?
                            <br>
                            we'll answer your problem here
                        </p>
                    </a>
                    <Socials/>
                </div>
                <div>
                    <h5 class="text-capitalize pb-2">support</h5>
                    <ul class="d-flex gap-2 m-0 list-unstyled flex-column">
                        <li v-for="(element) in supportArray">
                            <a :href="element.link">
                                <span>{{ element.name }}</span>
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h5 class="text-capitalize pb-2">about</h5>
                    <ul class="d-flex gap-2 m-0 list-unstyled flex-column">
                        <li v-for="(element) in aboutArray">
                            <a :href="element.link">
                                <span>{{ element.name }}</span>
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h5 class="text-capitalize pb-2">faq</h5>
                    <ul class="d-flex gap-2 m-0 list-unstyled flex-column">
                        <li v-for="(element) in faqArray">
                            <a :href="element.link">
                                <span>{{ element.name }}</span>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="d-flex flex-column gap-3">
                    <h5 class="text-capitalize">Contact me</h5>
                    <div class="d-flex align-items-center gap-3 pb-2">
                            <svg width="16" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                                <path fill="#CE7C2A" d="M429.6 92.1c4.9-11.9 2.1-25.6-7-34.7s-22.8-11.9-34.7-7l-352 144c-14.2 5.8-22.2 20.8-19.3 35.8s16.1 25.8 31.4 25.8H224V432c0 15.3 10.8 28.4 25.8 31.4s30-5.1 35.8-19.3l144-352z"/>
                            </svg>
                            <span class="info">
                                4500 Mercantile plaza, suite
                                <br>
                                300, fort worth, TX, 76137, USA
                            </span>
                        </div>
                    <div class="d-flex align-items-center gap-3 pb-2">
                            <svg width="16" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                                <path fill="#CE7C2A" d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"/>
                            </svg>
                            <span class="info">
                                +1(817)901 3377
                            </span>
                        </div>
                    <div class="d-flex align-items-center gap-3">
                        <svg width="16" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="#CE7C2A" d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/>
                        </svg>
                        <span class="info">
                            info@example.com
                        </span>
                    </div>
                </div>
            </div>
        </div>
        <div class="d-flex justify-content-center py-3">
            <a href="#">
                <span class="text-light">
                    Copyright 2022 by AttodogMilo.com
                </span>
            </a>
        </div>




        

    </div>

  


</template>








<style lang="scss" scoped>
    @import '../scss/styles.scss';
    #footerBg{
        position: relative;
        margin-top: 200px;
        padding-top: 200px;
        background-color: black;
        a,
        .info{
            color: #444444;
            &:hover{
                color: $primaryColor;
            }
        }
        h5{
            color: $primaryColor;
        }

        #floatingNews{
            margin-top: -325px;
            padding-bottom: 3rem;
            #emailField{
                position: relative;
                #emailPopup{
                    position: absolute;
                    background-color: #f4f4f4;
                    top: 107%;
                    border-radius: 10px;
                }
            }
        }
    
        #newsLetter{
            background-color: $primaryColor;
            border-radius: 10px;
            position: relative;
            div{
                padding-block: 4rem;
                div{
                    position: relative;
                    input{
                        border: none;
                        padding-block: 1rem;
                        padding-left: 1rem;
                    }
                    span{
                        position: absolute;
                        right: 5px;
                        bottom: 5px;
                        top: 5px;
                        background-color: $primaryColor;
                        padding: 3px;
                        cursor: pointer;
                        &:hover{
                            background-color: #7f7045;
                        }
                    }
                }
            }
            img{
                width: 45%;
                position: absolute;
                bottom: 0;
                left: 20px;
            }
        }
    }

    .v-enter-active,
    .v-leave-active {
        transition: opacity 1s ease;
    }

    .v-enter-from,
    .v-leave-to {
        opacity: 0;
    }




</style>