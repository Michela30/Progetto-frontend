<script>
//import

   export default {
    data() {
      return{
        //dati
        partners: [
            {
                name: 'paperplane',
                image: 'partner-1.png'
            },
            {
                name: 'medals',
                image: 'partner-2.png'
            },
            {
                name: '',
                image: 'partner-3.png'
            },
            {
                name: '',
                image: 'partner-4.png'
            },
            {
                name: 'school building',
                image: 'partner-5.png'
            },
            {
                name: 'handmade',
                image: 'partner-6.png'
            },
            {
                name: 'abc comunication',
                image: 'partner-7.png'
            },
            {
                name: '',
                image: 'partner-8.png'
            },
        ],

        linkListOne: [
            {
                title: 'Request a website',
                link: ''
            },
            {
                title: 'Browse Themes',
                link: ''
            },
            {
                title: 'Payment options',
                link: ''
            },
            {
                title: 'Support system',
                link: ''
            },
            {
                title: 'Checkout',
                link: ''
            },
            {
                title: 'Purchase theme',
                link: ''
            },
        ],

        linkListTwo: [
            {
                title: 'Purchase theme',
                link: ''
            },
            {
                title: 'Our Benefits',
                link: ''
            },
            {
                title: 'Our Team',
                link: ''
            },
            {
                title: 'Our Services',
                link: ''
            },
            {
                title: 'Other Products',
                link: ''
            },
            {
                title: 'My account',
                link: ''
            },
        ]
      }
    },
    methods: {
        //function
        getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        }
    },
    components: {
        //dichiarazione
    },
    props:{
        //utilizzo per file padre
    }
    
  }
</script>


<template>
    <footer>
        <section class="footer-top">
           <div class="text-center">
                <h2>
                    Partners
                </h2>

                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Non qui nesciunt eum voluptate? Corporis, in nulla!
                </p>
           </div>

           <div class="my_partner-row">

                <div class="partner-box" v-for="(singlePartner, i) in partners" :key="i">

                    <div class="img-box">
                        <img :src="getImagePath(`../assets/img/${singlePartner.image}`)" alt="">
                    </div>

                </div>
                
           </div>
        </section>

        
        <section class="footer-bottom">
            <div class="my_container">
                
                <div class="row justify-content-center">

                    <!-- footer logo/icon -->
                    <div class="col col-left">
                        <div class="logo-box">
                            img logo
                        </div>

                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. A, doloribus cumque? Sunt, dolor numquam!
                        </p>

                        <span>
                            icon
                        </span>
                        <span>
                            icon
                        </span>
                        <span>
                            icon
                        </span>
                    </div>

                    <!-- footer link -->
                    <div class="col col-middle">
                        <div class="d-flex">

                            <div class="list-one">
                                <span>
                                    Get EduPrime
                                </span>

                                <ul>
                                    <li v-for="(singleLinkOne, index) in linkListOne" :key="index">
                                        <a href="">
                                            {{singleLinkOne.title}}
                                        </a>
                                    </li>
                                </ul>
                            </div>

                            <div class="list-two">
                                <span>
                                    Networking
                                </span>

                                <ul>
                                    <li v-for="(singleLinkTwo, index) in linkListTwo" :key="index">
                                        <a href="">
                                            {{singleLinkTwo.title}}
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!-- footer search -->
                    <div class="col">
                        col 3
                    </div>
                </div>

            </div>
        </section>
    </footer>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.footer-top{
    background-color: white;
    padding: 40px 0;

    >* {
        padding: 10px 0;
    }

    p{
        font-size: 0.8em;
        width: 30%;
    }

    .my_partner-row{
        display: flex;
        justify-content: center;
        max-width: 800px;

        .partner-box{
            width: calc(100% / 8);
            .img-box{
                height: 40px;
                opacity: 0.3;
                
                img{
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }

            .img-box:hover{
                opacity: 1;
            }
        }
    }
}

.footer-bottom{
    padding: 70px 0 50px;
    background-color: $color-coral-primary;
    color: white;

    .col-left{
        .logo-box{
            //width: 180px;
            height: 50px;
            background-color: beige;
             
            img{
                width: 100%;
            }

        }
            p{
                padding-top: 10px;
                padding-left: 0;
                font-size: 0.8em;
            }
    }

    .col-middle{
        
        .list-one, .list-two{

            span{
                font-size: 0.8em;
            }
            ul{
                padding-left: 0;
                padding-top: 10px;

                li{
                    list-style-type: none;

                    a{
                        color: white;
                        text-decoration: none;
                        font-size: 0.6em;
                    }
                }
            }
        }
    }
}
</style>