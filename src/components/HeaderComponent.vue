<script>
//import

   export default {
    data() {
      return{
        //dati
        navBarLink: [
            {
                title: 'Home',
                link: '',
                hasDropdown: true
            },
            {
                title: 'Courses',
                link: '',
                hasDropdown: true
            },
            {
                title: 'About Us',
                link: '',
                hasDropdown: false
            },
            {
                title: 'News',
                link: '',
                hasDropdown: true
            },
            {
                title: 'Pages',
                link: '',
                hasDropdown: true
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
        
      }
    },
    methods: {
        //function
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
    
    <header>
       <div class="header-top">

            <div class="d-flex">
                <div class="col-4">
                    logo
                </div>

                <nav class="col-8">
                    <ul class="dropdown">

                        <li class="link-nav" v-for="(singleLink, i) in navBarLink" :key="i">
                            <a href="#" :class="{'dropdown-toggle' : singleLink.hasDropdown == true}" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                                {{singleLink.title}}
                            </a>
                                    
                            <ul :class="{'dropdown-menu': singleLink.hasDropdown == true,
                                        'd-none': singleLink.hasDropdown == false,}">
                                <li><a :class="{'dropdown-item' : singleLink.hasDropdown == true}" href="#">Action</a></li>
                                <li><a :class="{'dropdown-item' : singleLink.hasDropdown == true}" href="#">Another action</a></li>
                                <li><a :class="{'dropdown-item' : singleLink.hasDropdown == true}" href="#">Something else here</a></li>
                            </ul>
                        </li>

                        <button>
                            button component
                        </button>
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
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus autem fuga mollitia ullam consequuntur.
                    </p>
    
                    <div class="d-flex justify-content-center">
                        <button>
                            button comp giallo
                        </button>
    
                        <button>
                            button comp white
                        </button>
                        
                    </div>
                </div>
                
            </div>

            <div>
                button in absolute
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

    nav {
        .dropdown {
           
            .link-nav {
                display: inline-block;
                padding: 0 10px;
                list-style-type: none;
                a {
                    color: white;
                    text-decoration: none;

                }

                a:hover{
                    color: $color-yellow;
                }
            }
        }
    }
    button {
        margin-left: 5px;
    }
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