<script>
//import
import myButton from './myButton.vue';


   export default {
    data() {
      return{
        //dati
        latestCourses: [
            {
                image: 'img/Decisions-icon.png',
                title: 'Make Better Decisions',
                teacher: 'James Collins',
                price: '$21.00'
            },
            {
                image: 'img/Speaker-icon.png',
                title: 'How to be a speaker',
                teacher: 'James Collins',
                price: 'Free'
            },
            {
                image: 'img/Network-icon.png',
                title: 'Network Introductions',
                teacher: 'James Collins',
                price: 'Free'
            },
            {
                image: 'img/Brand-icon.png',
                title: 'Brand Management',
                teacher: 'James Collins',
                price: 'Free'
            }
        ],
        buttonEight: {
            title: 'View Course',
            color: 'button-coral',
            icon: 'fa solid fa-eye fa-xs',
        },
        buttonNine: {
            title: 'Discover the Method',
            color: 'button-coral',
            icon: null,
        },
        buttonTen: {
            title: 'List of Fees',
            color: 'button-coral',
            icon: null,
        }
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
        myButton
    },
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>
    
    <section class="third-section">

       <div class="wave-bottom ms-0">
            <img class="sfondo" src="../assets/svg/svg-1.svg" alt="">
        </div>

    <!-- first part: courses -->

        <div class="my_container px-4">
            <h2 id="courses">
                Latest Courses
            </h2>

            <div class="row pt-4 gx-2">

                <div class="col" v-for="(singleCourse, i) in latestCourses" :key="i">
                    <div class="icon-box">
                        <img :src="singleCourse.image">
                    </div>
                    <h6 class="title">
                        {{singleCourse.title}}
                    </h6>

                    <div class="teacher">
                        <i class="fa-xs fa-regular fa-user"></i>
                        <span>
                            Teacher:
                        </span>
                        <strong><small>
                            {{singleCourse.teacher}}
                        </small></strong>
                    </div>

                    <div class="price">
                        <i class="fa-xs fa-solid fa-money-bill-1"></i>
                        <span>
                            Price:
                        </span>
                        <strong><small>
                            {{singleCourse.price}}
                        </small></strong>
                    </div>

                    <span class="buttonEight">
                        <myButton
                        :title="buttonEight.title"
                        :color="buttonEight.color"
                        :icon="buttonEight.icon"/>
                    </span>

                </div>
            </div>

            <!-- second part: exam  -->

            <div class="row my_row">
                <div class="col-7">

                    <div class="text-col">
                        <div class="icon-section">
                            <img src="../assets/img/Exam-icon.png" alt="">
                        </div>
                        <h2>
                            The most efficient examination method
                        </h2>
                        <p>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, doloribus aspernatur numquam nobis odit possimus consequuntur quod a tenetur nemo. Quibusdam delectus hic reprehenderit explicabo possimus repudiandae obcaecati nihil nobis.
                        </p>
                        <div class="buttonNine">
                            <myButton
                            :title="buttonNine.title"
                            :color="buttonNine.color"/>
                        </div>
                    </div>
                </div>

                <div class="col-5">
                    <div class="image-box">
                        <img src="../assets/img/Exam-Illustration.png" alt="">
                    </div>

                </div>
            </div>

             <!-- second part: variable fees  -->

             <div class="row my_row">

                <div class="col-5">
                    <div class="image-box">
                        <img src="../assets/img/Girl-Illustration.png" alt="">
                    </div>
                </div>

                <div class="col-7">

                <div class="text-col ps-3">
                    <div class="icon-section">
                        <img src="../assets/img/Exam-icon-1.png" alt="">
                    </div>
                    <h2>
                        Variable fees for international student
                    </h2>
                    <p>
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sit, doloribus aspernatur numquam nobis odit possimus consequuntur quod a tenetur nemo. Quibusdam delectus hic reprehenderit explicabo possimus repudiandae obcaecati nihil nobis.
                    </p>
                    <div class="buttonNine">
                        <myButton
                        :title="buttonTen.title"
                        :color="buttonTen.color"/>
                    </div>
                </div>
                </div>
            </div>
        </div>
        
   </section>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.third-section{
    background-color: white;
    padding: 0 0 40px;

    .col{
        padding: 5px 10px;
        margin: 0 10px;
        border: 1px solid #F7F8FA;
        text-align: center;
        height: 200px;
        box-shadow: 0px 2px 13px 6px #F7F8FA;
        position: relative;
        .icon-box{
            margin-top: 15px;
            width: 50px;
            height: 50px;
            
            img {
                width: 100%;
            }
        }

        .title{
            padding-top: 15px;
            font-weight: bolder;
        }

        .teacher, .price{
            padding-top: 5px;

            span{
                font-size: 0.8em;
            }
            strong{
                font-size: 0.8em;
            }
        }

    }

    .my_row{

        margin-top: 70px;
        .col-7 > *{
            padding: 15px 0px;
            
            .icon-section{
                width: 50px;
                height: 50px;
                margin: 0;
                
                img{
                    width: 100%;
                }
            }
    
        }
    }
    
    .text-col{
        h2{
            padding: 10px 0;
            padding-right: 100px;
        }

        p{
            padding-right: 120px;
            font-size: 0.8em;
        }
    }
    .image-box{
        padding-right: 50px;
        margin-top: 60px;
        width: 350px;

        img{
            width: 100%;
        }
    }

    .wave-bottom{
        img{
            width: 100%;
            margin-top: -1px;
        }
    }
   
}
</style>