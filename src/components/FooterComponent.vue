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
        ],

        linkFooterRight: [
            {
                title: 'economy',
                link: ''
            },
            {
                title: 'design',
                link: ''
            },
            {
                title: 'coaching',
                link: ''
            },
            {
                title: 'business',
                link: ''
            },
            {
                title: 'medicine',
                link: ''
            },
            {
                title: 'law',
                link: ''
            },
            {
                title: 'fitness',
                link: ''
            }
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
            <div class="sfondo">
                <div class="bg">

                </div>
            </div>
        </section>

        
        <section class="footer-bottom">
            <div class="my_container">
                
                <div class="row justify-content-center">

                    <!-- footer logo/icon -->
                    <div class="col col-left">
                        <div class="logo-box">
                            <img src="../assets/img/theme_eduprime_logo.png" alt="">
                        </div>

                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. A, doloribus cumque? Sunt, dolor numquam!
                        </p>

                        <div class="social">

                            <a href="https://www.facebook.com/login/" target="_blank">
                                <i class="fa-xs fa-brands fa-facebook-f"></i>
                            </a>
                            <a href="https://twitter.com/i/flow/login" target="_blank">
                                <i class="fa-xs fa-brands fa-twitter"></i>
                            </a>
                            <a href="https://www.instagram.com/accounts/login/" target="_blank">
                                <i class="fa-xs fa-brands fa-instagram"></i>
                            </a>

                        </div>
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
                    <div class="col col-right">
                        
                        <form action="">
                            <div class="input-group">
                                <input type="text" class=" rounded-pill border border-none ps-2 w-100" placeholder="Search..." aria-label="Search" aria-describedby="button-addon2">

                                <button class="btn rounded-circle send-button" type="submit" id="button-addon2">
                                    <i class="fa-xs fa-solid fa-magnifying-glass"></i>
                                </button>
                            </div>
                        </form>

                        <div class="col-right-text">
                            <div>
                                <strong class="title">
                                    Search categories
                                </strong>
                            </div>

                            <div class="categories" v-for="singleLinkFooter in linkFooterRight">
                                <a href="#">
                                    {{singleLinkFooter.title}}
                                </a>
                            </div>

                            <div>
                                <a href="#" id="copyright">
                                    ModelTheme@poweredbyMichela
                                </a>
                            </div>
                        </div>

                    </div>
                </div>

            </div>

            <div class="button-to-top">
                <button>
                    <a href="#">
                        <i class="fa-solid fa-arrow-up"></i>
                    </a>
                </button>
            </div>
        </section>
    </footer>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.footer-top{
    background-color: white;
    padding: 40px 0 0;

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

    .sfondo{
    
        background-image: url(../assets/img/background-wave3.png);
        height: 200px;
        width: 100%;
        background-position: top right;
        filter: invert(0.1);
        transform: rotate(180deg);
        
        .bg{
            width: 100%;
            height: 100%;
            object-fit: scale-down;
        }
    }
}

.footer-bottom{
    padding: 70px 0 50px;
    background-color: $color-coral-primary;
    color: white;
    position: relative;

    .col-left{
        .logo-box{
            width: 180px;
            height: 50px;
            margin-left: 0;
             
            img{
                width: 100%;
            }

        }
            p{
                padding-top: 10px;
                padding-left: 0;
                font-size: 0.8em;
            }

        .social{
            >*{
                margin-right: 10px;
            }
            a{
                color: white;

                i{
                    line-height: 17px;
                    height: 30px;
                    width: 30px;
                    border-radius: 50%;
                    border: 1px solid $color-yellow;
                    padding: 5px 10px;
                }
            }
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

            li a:hover{
                color: $color-yellow;
                text-decoration: underline;
            }
        }
    }

    .col-right{
        form{
        margin-left: 35px;

        input{
            height: 40px;
            font-size: 0.6em;
            position: relative;
        }

        .send-button{
            background-color: $color-yellow;
            height: 40px;
            width: 40px;
            border-radius: 50%;
            position: absolute;
            right: -10px;
            color: white;
            box-shadow: -20px -1px 31px -11px #F7F8FA;
            }
        }

        .col-right-text{
            text-align: right;
            margin-top: 15px;

            >*{
                padding: 5px 0;
            }

            .title{
                font-size: 0.8em;
            }
            
            .categories{
                font-size: 0.7em;
                text-transform: uppercase;
                display: inline-block;

                >*{
                    text-decoration: none;
                    color: white;
                    margin-left: 15px;
                    border: 1px solid white;
                    height: 20px;
                    width: 40px;
                    border-radius: 20px;
                    padding: 0 10px;
                }
            }

            .categories a:hover{
                background-color: $color-yellow;
            }

            #copyright{
                text-decoration: none;
                font-size: 0.6em;
                color: $color-yellow;
            }
        }
    }

    .button-to-top{
        background-color: $color-yellow;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        position: fixed;
        right: 30px;
        bottom: 20px;
        
        button{
            border: none;
            background-color: transparent;
            
            a{
                color: white;
                margin-left: 14px;
               
                i{
                    margin-top: 12px;
                }
            }
        }
    }
}
</style>