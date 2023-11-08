<script>
//import
import myButton from './myButton.vue';

   export default {
    data() {
      return{
        //dati
        count: 0,
        faculties: [
            {
                image: 'img/Gavel-v2.png',
                link: '',
                title: 'Law Faculty'
            },
            {
                image: 'img/Coins-tabs-v2.png',
                link: '',
                title: 'Economy'
            },
            {
                image: 'img/Medicine-tabs-v2.png',
                link: '',
                title: 'Medicine'
            },
            {
                image: 'img/Computer-tabs-v2.png',
                link: '',
                title: 'Computer Science'
            },
            {
                image: 'img/Palette-tabs-v2.png',
                link: '',
                title: 'Graphic Design'
            }
        ],
        facultiesDescription: [
            {
                image: 'img/Gavel-Illustration-e1556884768193.png',
                title: 'Law Faculty',
                text: '   Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium deserunt voluptatibus obcaecati harum voluptatum. Ipsam nisi molestiae ab impedit, suscipit libero dolor totam optio pariatur aut, quibusdam assumenda atque tempore natus porro unde illum laborum quisquam dignissimos deserunt. Quisquam, maiores!'
            },
            {
                image: 'img/Economy.png',
                title: 'Economy',
                text: '   Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium deserunt voluptatibus obcaecati harum voluptatum. Ipsam nisi molestiae ab impedit, suscipit libero dolor totam optio pariatur aut, quibusdam assumenda atque tempore natus porro unde illum laborum quisquam dignissimos deserunt. Quisquam, maiores!'
            },
            {
                image: 'img/Medicine.png',
                title: 'Medicine',
                text: '   Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium deserunt voluptatibus obcaecati harum voluptatum. Ipsam nisi molestiae ab impedit, suscipit libero dolor totam optio pariatur aut, quibusdam assumenda atque tempore natus porro unde illum laborum quisquam dignissimos deserunt. Quisquam, maiores!'
            },
            {
                image: 'img/Computer-Science.png',
                title: 'Computer Science',
                text: '   Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium deserunt voluptatibus obcaecati harum voluptatum. Ipsam nisi molestiae ab impedit, suscipit libero dolor totam optio pariatur aut, quibusdam assumenda atque tempore natus porro unde illum laborum quisquam dignissimos deserunt. Quisquam, maiores!'
            },
            {
                image: 'img/Graphic-Design.png',
                title: 'Graphic Design',
                text: '   Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium deserunt voluptatibus obcaecati harum voluptatum. Ipsam nisi molestiae ab impedit, suscipit libero dolor totam optio pariatur aut, quibusdam assumenda atque tempore natus porro unde illum laborum quisquam dignissimos deserunt. Quisquam, maiores!'
            }
        ],

        buttonFour: {
            title: 'Browse through courses',
            color: 'button-yellow',
            icon: null,
        },
        buttonFive: {
            title: 'Read More',
            color: 'button-coral',
            icon: null,
        }
      }
    },
    methods: {
        //function
        getImagePath: function(image){
            return new URL (image, import.meta.url).href;
        },
        nextTab(index){

            this.count = index;
        },
    },
    components: {
        //dichiarazione
        myButton
    },
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>

    <!-- first section -->
    <section class="first-section">

        <div class="sfondo-dx">

            <div class="my_container" id="first-course">
                
                <div class="row">
                    <div class="col-8">
                        
                        <div class="icon-section">
                            <img src="../assets/img/Books-icon.png" alt="">
                        </div>
                        <h2>
                            Thousand of courses for any type of student
                        </h2>
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem similique nulla praesentium debitis velit cumque doloremque culpa eligendi ipsam, asperiores nesciunt! Natus, debitis? Maiores quod cumque voluptates dolorum 
                        </p>
                        <span class="buttonFour">
                            <myButton
                            :title="buttonFour.title"
                            :color="buttonFour.color"/>
                        </span>
                        
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

        </div>


        <div class="my-small-container text-center" id="faculties">
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
                    <!-- slider -->

                    <div class="col" v-for="(iconFaculties, index) in faculties" :key="index" @click="nextTab(index)">
                        <div class="iconFaculties-box">
                            <img :src="iconFaculties.image">
                        </div>
                        <strong>
                            {{iconFaculties.title}}
                        </strong>

                    <div class="triangle">
                        
                    </div>
                </div>
                
                <div class="col">
                    
                </div>
            </div>
        </div>

        <div class="faculty-description" :class="(i == count) ? 'd-block' : 'd-none' " v-for="(singleTab,i) in facultiesDescription" :key="i" tabindex="0">
            
            <div class="row justify-content-center">
                <div class="col-5">

                    <div class="faculty-img">
                        <img :src="singleTab.image" alt="">
                    </div>

                </div>

                <div class="col-7">
                    <h2>
                        {{singleTab.title}}
                    </h2>

                    <p>
                        {{singleTab.text}}
                    </p>

                    <span class="buttonFive">
                        <myButton
                        :title="buttonFive.title"
                        :color="buttonFive.color"/>
                    </span>

                </div>
            </div>
        </div>
        
        <div class="wave-bottom">
            <img src="../assets/svg/svg-0.svg" alt="">
        </div>
    </section>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.first-section{
    padding-top: 80px;

    .icon-section{
        width: 50px;
        height: 50px;
        margin-left: 70px;
        
        img{
            width: 100%;
        }
    }

    .col-8{

        height: auto;
        h2, p{
           padding: 15px 70px;
       }
    }

    .image-box{
        padding-right: 50px;
        margin-left: 0;
        margin-top: 50px;
        width: 350px;

        img{
            width: 100%;
        }
    }

    .my-small-container{
        margin-top: 20px;

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
        position: relative;

        .iconFaculties-box{
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
    .col:hover{
        background-color: $color-coral-primary;
        color: white;
        
        .triangle{
            width: 10px;
            height: 10px;
            border-left: 1px solid $color-coral-primary;
            border-bottom: 1px solid $color-coral-primary;
            background-color: $color-coral-primary;
            transform: rotate(315deg);
            position: absolute;
            bottom: -5px;
            left: 90px;
        }

        strong{
            color: white;
        }
        .iconFaculties-box{
            filter: brightness(250%);
        }
    }

    .faculty-description{
        padding: 80px 0 30px;
        max-width: 900px;
        .faculty-img{
            padding: 10px;
            width: 300px;

            img{
                width: 100%;
            }
        }

        .col-7 {
            h2,p{
                padding: 10px;
            }
            button{
                margin-left: 10px;
            }
        }
    }

    .wave-bottom{
        img{
            width: 100%;
            margin-bottom: -1px;
        }
    }
}

.sfondo-dx{
    background-image: url(../assets/img/home-background.png);
    background-size: cover;
    height: 420px;
    color: grey;
}
</style>