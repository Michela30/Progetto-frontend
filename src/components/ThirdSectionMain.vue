<script>
//import

   export default {
    data() {
      return{
        //dati
        latestCourses: [
            {
                image: 'Decisions-icon.png',
                title: 'Make Better Decisions',
                teacher: 'James Collins',
                price: '$21.00'
            },
            {
                image: 'Speaker-icon.png',
                title: 'How to be a speaker',
                teacher: 'James Collins',
                price: 'Free'
            },
            {
                image: 'Network-icon.png',
                title: 'Network Introductions',
                teacher: 'James Collins',
                price: 'Free'
            },
            {
                image: 'Brand-icon.png',
                title: 'Brand Management',
                teacher: 'James Collins',
                price: 'Free'
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
    
    <section class="third-section">

       <div class="wave-bottom ms-0">
            <img class="sfondo" src="../assets/svg/svg-1.svg" alt="">
        </div>

    <!-- first part: courses -->

        <div class="my_container px-4">
            <h2>
                Latest Courses
            </h2>

            <div class="row pt-4 gx-2">

                <div class="col" v-for="(singleCourse, i) in latestCourses" :key="i">
                    <div class="icon-box">
                        <img :src="getImagePath(`../assets/img/${singleCourse.image}`)">
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

                    <button>
                        view course
                    </button>

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
                        <button>
                            comp yellow button
                        </button>
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
                    <button>
                        comp yellow button
                    </button>
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
        }
    }
   
}
</style>