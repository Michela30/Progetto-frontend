<script>
//import
import myButton from './myButton.vue';

   export default {
    data() {
      return{
        //dati
        events: [
            {
                title: 'Coaching Session',
                time: '20 May 21.30 PM',
                text: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga nam, fugiat aut quidem laboriosam mollitia.'
            },
            {
                title: 'Coaching Session',
                time: '24 Mar 18:00 PM',
                text: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga nam, fugiat aut quidem laboriosam mollitia.'
            },
            {
                title: 'Coaching Session',
                time: '12 Feb 13.30 PM',
                text: ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga nam, fugiat aut quidem laboriosam mollitia.'
            }
        ],
        buttonSix: {
            title: 'Find More',
            color: 'button-coral',
            icon: 'fa solid fa-plus fa-xs',
        },
        buttonSeven: {
            title: 'View all events',
            color: 'button-yellow',
            icon: null,
        }
      }
    },
    methods: {
        //function
      
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

   <section class="second-section">

    <!-- prima parte della section: university-->

        <div class="uni-section">
            
            <div class="text-center">

                <div class="icon-section">
                    <img src="../assets/img/Clock-and-Bell.png" alt="">
                </div>

                <h2>
                    University Year
                </h2>

                <!-- paragrafi della timeline -->
                <div class="d-flex paragraphs-top">
                    <div class="firstpar">
                        <strong>
                            Demo Classes
                        </strong>
                        <p>
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque consectetur unde obcaecati eaque.
                        </p>
                    </div>
                    <div class="secondpar">
                        <strong>
                            Graduation Day
                        </strong>
                        <p>
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque consectetur unde obcaecati eaque.
                        </p>
                    </div>
                </div>

                <!-- timeline -->
                <div class="timeline">
                    <img src="../assets/img/Timeline-Item.png" alt="">
                </div>

                <!-- paragrafi della timeline -->
                <div class="d-flex paragraphs-bottom">
                    <div class="thirdpar">
                        <strong>
                            Orientation
                        </strong>
                        <p>
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque consectetur unde obcaecati eaque.
                        </p>
                    </div>
                    <div class="fourthpar">
                        <strong>
                            Evaluation
                        </strong>
                        <p>
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque consectetur unde obcaecati eaque.
                        </p>
                    </div>
                </div>
            </div>
            
        </div>

    <!-- seconda parte della section: events -->

        <div class="events">
            <div class="text-center">
                <div class="icon-section">
                    <img src="../assets/img/upcoming-events-calendar-icon.png" alt="">
                </div>

                <h2>
                    Upcoming Events
                </h2>

                <div class="row justify-content-center">
                    <div class="my_card" v-for="(singleCard, i) in events" :key="i">
                        <h5>
                            {{ singleCard.title }}
                        </h5>

                        <i class="fa-regular fa-calendar-days fa-xs"></i>

                        <span class="time">
                            {{ singleCard.time }}
                        </span>

                        <p>
                            {{ singleCard.text }}
                        </p>

                        <div class="buttonSix">
                            <myButton
                            :title="buttonSix.title"
                            :color="buttonSix.color"
                            :icon="buttonSix.icon"/>
                        </div>
                    </div>
                    
                </div>

                <div class="buttonSeven">
                    <myButton
                    :title="buttonSeven.title"
                    :color="buttonSeven.color"/>
                </div>
            </div>
        </div>

        
   </section>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.second-section{
    background-color: $color-coral-primary;

    .icon-section{
        width: 50px;
        height: 50px;
        margin-bottom: 15px;
        
        img{
            width: 100%;
        }
    }

    .uni-section{
        padding: 40px 0;
        color: white;

        h2{
            background-color: $color-red;
            width: 250px;
            text-align: center;
        }
        .paragraphs-top{
            >*{
                text-align: center;
                width: 20%;
                padding-top: 50px;

                p{
                    font-size: 0.6em;
                }
            }
            .firstpar{
                margin-left: 430px;
            }
            .secondpar{
                margin-right: 230px;
            }
        }

        .paragraphs-bottom{
            >*{
                text-align: center;
                width: 20%;
                padding-top: 20px;

                p{
                    font-size: 0.6em;
                }
            }
            .thirdpar{
                margin-left: 250px;
            }
            .fourthpar{
                margin-right: 420px;
            }
        }

        .timeline{
            padding-top: 20px;
            width: 900px;

            img{
                width: 100%;
            }
        }
    }

    .events{
        padding: 40px 0;
        color: white;

        .my_card{
            margin: 30px 20px 0;
            width: 250px;
            border-radius: 30px;
            background-color: white;
            color: black;
            padding: 25px 10px;
            position: relative;
            
            p{
                font-size: 0.7em;
            }
            
            .time{
                font-size: 0.6em;
                padding-left: 5px;
            }
        }
    }
}


</style>