<script>
    import Socials from './Header/Socials.vue'
    export default {
        name: "HeaderComponent",
        components:{
            Socials,
        },
        data(){
            return{
                navArray:[
                    {
                        name: 'home',
                        link: '#'
                    },
                    {
                        name: 'about',
                        link: '#'
                    },
                    {
                        name: 'services',
                        link: '#'
                    },
                    {
                        name: 'training',
                        link: '#'
                    },
                    {
                        name: 'blogs',
                        link: '#'
                    },
                ]
            }
        },
    }
</script>






<template>
  
    <header>
        <div id="topHeaderBg">
            <div id="topHeaderItems" class="w-50 m-auto text-light d-flex justify-content-between py-3">
                <div id="topHeaderLeft" class="d-flex gap-5">
                    <div id="emailInfo" class="d-flex align-items-center gap-2">
                        <svg width="16" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="#CE7C2A" d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/>
                        </svg>
                        <span>
                            info@example.com
                        </span>
                    </div>
                    <div id="phoneInfo" class="d-flex align-items-center gap-1">
                        <svg width="16" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="#CE7C2A" d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"/>
                        </svg>
                        <span>
                            +1(817)901 3377
                        </span>
                    </div>
                </div>
                <div id="topHeaderRight">
                    <Socials/>
                </div>
            </div>
        </div>
        <div id="bottomHeaderBg">
            <div id="bottomHeaderItems" class="w-50 m-auto text-light py-3 d-flex justify-content-between align-items-center">
                <img src="../assets/img/logo.png" alt="siteLogo">
                <div class="d-flex align-items-center gap-4">
                    <nav>
                        <ul class="d-flex gap-3 m-0">
                            <li class="text-black" v-for="(element) in navArray">
                                <a :href="element.link">
                                    <span>{{ element.name }}</span>
                                </a>
                            </li>
                        </ul>
                    </nav>
                    <a href="#" class="primaryButton">
                        <span>
                            get in touch!
                        </span>
                    </a>
                </div>
            </div>
        </div>
    </header>

  


</template>








<style lang="scss" scoped>
    @import '../scss/styles.scss';
    #topHeaderBg{
        background-color: #7F7045;
    }

    li{
        list-style-type: none;
        a{
            text-decoration: none;
            color: #847F82;
            text-transform: capitalize;
            font-weight: 600;
            font-size: 20px;
            &:hover{
                color: $primaryColor;
            }
        }
    }



</style>