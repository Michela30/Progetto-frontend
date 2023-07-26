<script>
//import
import myButton from './myButton.vue';

   export default {
    data() {
      return{
        //dati
        navBarLink: [
            {
                title: 'Home',
                link: '',
                hasDropdown: true,

                linkDropdown: [
                    {
                        title: 'Events',
                        link: '#event'
                    },
                    {
                        title: 'Latest Courses',
                        link: '#courses'
                    },
                ]

            },
            {
                title: 'Courses',
                link: '',
                hasDropdown: true,
                linkDropdown: [
                    {
                        title: 'All the Faculties',
                        link: '#faculties'
                    },
                    {
                        title: 'Law Faculty',
                        link: ''
                    },
                    {
                        title: 'Economy',
                        link: ''
                    },
                    {
                        title: 'Medicine',
                        link: ''
                    },
                    {
                        title: 'Computer Science',
                        link: ''
                    },
                    {
                        title: 'Grapich Design',
                        link: ''
                    }
                ]
            },
            {
                title: 'About Us',
                link: '',
                hasDropdown: false
            },
            {
                title: 'News',
                link: '',
                hasDropdown: true,

                linkDropdown: [
                    {
                        title: 'Blog',
                        link: ''
                    },
                ]
            },
            {
                title: 'Pages',
                link: '',
                hasDropdown: true,

                linkDropdown: [
                    {
                        title: 'Courses',
                        link: '#first-course'
                    },
                    {
                        title: 'University Year',
                        link: '#university'
                    }
                ]
            },
            {
                title: 'Contact',
                link: '',
                hasDropdown: false
            },
            {
                title: 'Purchase',
                link: '',
                hasDropdown: false
            }            
        ],
        
        buttonUno: {
            title: 'VIEW COURSES',
            color: 'button-yellow',
            icon: null,
        }, 
        buttonDue: {
            title: 'Search Courses',
            color: 'button-yellow',
            icon: 'fa solid fa-magnifying-glass fa-xs',
        },
        buttonTre: {
            title: 'Apply for university',
            color: 'button-white',
            icon: 'fa solid fa-user-plus fa-xs',
        }
        
      }
    },
    methods: {
        //function
    },
    components: {
        //dichiarazione
        myButton,
    },
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>
    
    <header>
        
        
       <div class="header-top">

            <div class="d-flex">
                <div class="col-4">
                   
                    <div class="logo-box">
                        <img src="../assets/img/theme_eduprime_logo.png" alt="">
                    </div>

                </div>

                <nav class="col-8">
                    <ul class="dropdown">

                        <li class="link-nav" v-for="(singleLink, i) in navBarLink" :key="i">
                            <a id="navbar-a" :href="singleLink.link" :class="{'dropdown-toggle' : singleLink.hasDropdown == true}" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                                {{singleLink.title}}
                            </a>

                            
                            <ul :class="{'dropdown-menu': singleLink.hasDropdown == true,
                                        'd-none': singleLink.hasDropdown == false,}">

                                <li v-for="(singleLinkDropdown, index) in navBarLink[i].linkDropdown" :key="index">
                                    <a :class="{'dropdown-item' : singleLink.hasDropdown == true}" :href="singleLinkDropdown.link">
                                        {{singleLinkDropdown.title}}
                                    </a>
                                </li>
                            </ul>
                                    
                        </li>

                        <span class="header-top-button">
                            <a href="#courses">
                                <myButton
                                :title="buttonUno.title"
                                :color="buttonUno.color"/>
                            </a>
                        </span>
                    </ul>
                </nav>
            </div>

       </div>

       <div class="header-bottom">
        
       <div class="wave">
            <img src="../assets/img/Wave-1.png" alt="">
       </div>
            <div class="my-small-container text-center">
                
                <div class="jumbotron-text">
                    <h1>
                        Key to your success
                    </h1>
    
                    <p>
                        EduPrime is the most versatile Wordpress theme for educational purposes, showcasing universities, courses, secondary schools etc
                    </p>
    
                    <div class="d-flex justify-content-center">

                        <span class="buttonDue">
                            <myButton
                            :title="buttonDue.title"
                            :color="buttonDue.color"
                            :icon="buttonDue.icon"/>
                        </span>
    
                        <span class="buttonTre">
                            <myButton
                            :title="buttonTre.title"
                            :color="buttonTre.color"
                            :icon="buttonTre.icon"/>
                        </span>
                        
                    </div>
                </div>
                
            </div>

            <div class="icon--header-left">
               <div class="d-flex flex-column">
                    <a href="#" class="text-white">
                        <i class="fa-xs fa-solid fa-cart-shopping"></i>
                    </a>
                    <a href="#" class="text-white">
                        <i class="fa-xs fa-regular fa-map"></i>
                    </a>
                    <a href="#" class="text-white">
                        <i class="fa-xs fa-solid fa-life-ring"></i>
                    </a>
               </div>
            </div>
       </div>

  
    </header>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

header{
    color: white;
    height: 590px;
    background-image: url(../assets/img/theme_slider2_bg-1.jpg);
    background-position-y: top;
    background-size: cover;
    background-repeat: no-repeat;
    
    .header-top, .header-bottom{
        background-color: rgba(222,111,112,0.9);

    }
    .header-bottom{
        height: 510px;
        position: relative;

        .jumbotron-text {
            padding-top: 100px;

            >* {
                padding: 15px 0;
            } 
        }
    }

}
.header-top {
    padding: 40px 40px 5px;

    .logo-box{
        padding-bottom: 30px;
        width: 180px;
        height: 40px;

        img{
            width: 100%;
        }
    }

    nav {
        .dropdown {
           
            .link-nav {
                display: inline-block;
                padding: 0 10px;
                list-style-type: none;
                #navbar-a {
                    color: white;
                    text-decoration: none;

                }
                #navbar-a:hover{
                    color: $color-yellow;
                }

            }
        }
    }

    .logo-box,nav{
        line-height: 40px;
    }
    .my_dropdown{
        li{
            a{
                color: black;
            }
        }
    }
    button {
        margin-left: 5px;
    }
}
.icon--header-left{
    background-color: $color-yellow;
    width: 25px;
    position: absolute;
    top: 150px;
    box-shadow: 19px 4px 40px -10px #000000;
}
.wave{
    width: 100%;

    img{
        width: 100%;
        position: absolute;
        bottom: 0px;
        object-fit: cover;
    }
}


</style>