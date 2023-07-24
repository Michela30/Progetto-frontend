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
            },
        ]
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

       </div>
    </header>

</template>



<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.header-top {
    padding: 20px 40px;

    nav {
        .dropdown {
           
            .link-nav {
                display: inline-block;
                padding: 0 10px;
                list-style-type: none;
                a {
                    color: black;
                    text-decoration: none;
                }
            }
        }
    }
    button {
        margin-left: 5px;
    }
}
</style>