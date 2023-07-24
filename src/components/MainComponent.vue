<script>
//import

   export default {
    data() {
      return{
        //dati
        faculties: [
            {
                image: 'Gavel-v2.png',
                title: 'Law Faculty'
            },
            {
                image: 'Coins-tabs-v2.png',
                title: 'Economy'
            },
            {
                image: 'Medicine-tabs-v2.png',
                title: 'Medicine'
            },
            {
                image: 'Computer-tabs-v2.png',
                title: 'Computer Science'
            },
            {
                image: 'Palette-tabs-v2.png',
                title: 'Graphic Design'
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

    <main>
      <!-- first section -->
        <section class="first-section">
            <div class="my_container">
                
                <div class="row">
                    <div class="col-8">

                        <div>
                            <div class="icon">
                                <img src="../assets/img/Books-icon.png" alt="">
                            </div>
                            <h2>
                                Thousand of courses for any type of student
                            </h2>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem similique nulla praesentium debitis velit cumque doloremque culpa eligendi ipsam, asperiores nesciunt! Natus, debitis? Maiores quod cumque voluptates dolorum 
                            </p>
                            <button>
                                comp yellow button
                            </button>
                        </div>
                    </div>

                    <div class="col-4">
                        <div class="image-box">
                            <img src="../assets/img/Graduation-Illustration.png" alt="">
                        </div>

                        <!-- <div class="sfondo">

                        </div> -->
                    </div>
                </div>
            </div>


            <div class="my-small-container text-center">
                <h2>
                    Faculties available at EduPrime
                </h2>

                <p>
                    A single university with a load of courses, tailored to saisfy any student's needs
                </p>
            </div>


            <div>
                <div class="row">
                    <div class="col">
                        
                    </div>

                    <div class="col" v-for="icon in faculties">
                        <div class="icon-box">
                            <img :src="getImagePath(`../assets/img/${icon.image}`)">
                        </div>
                        <strong>
                            {{icon.title}}
                        </strong>
                    </div>
                    
                    <div class="col">
                        
                    </div>
                </div>
            </div>
        </section>
    </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.first-section{
    padding: 80px 0;

    .icon{
        width: 50px;
        height: 50px;
        margin: 0;
        
        img{
            width: 100%;
        }
    }

    .col-8 > *{
        padding: 15px 70px;
    }

    // .col-4 {
    //     position: relative;
    //     .sfondo {
    //         background-image: url(../assets/img/home-background.png);
    //         color: grey;
    //         background-position: right;
    //         background-repeat: no-repeat;
    //         background-size: cover;
    //         width: 300px;
    //         height: 400px;
    //         position: absolute;
    //         right: 0;
    //         top: 0;
    //     }
    // }

    .image-box{
        padding-right: 50px;
        margin-left: 0;
        margin-top: 50px;
        width: 350px;
        height: 450px;

        img{
            width: 100%;
        }
    }

    .my-small-container{
        p{
            padding: 10px 150px;
            font-size: 0.8em;
        }
    }

    .col{
        border: 1px solid #F7F8FA;
        text-align: center;
        height: 150px;
        box-shadow: 0 10px 10px #F7F8FA;

        .icon-box{
            padding: 25px 0 10px;
            width: 80px;
            height:auto;

            img{
                width: 100%;
            }
        }
        
        strong{
            color: $color-coral-primary;
            font-size: 0.8em;
        }
    }
}
</style>