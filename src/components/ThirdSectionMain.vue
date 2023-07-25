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

        <div class="my_container px-4">
            <h2>
                Latest Courses
            </h2>

            <div class="row">
                
            </div>
        </div>
        
   </section>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.third-section{
    background-color: white;
    padding: 40px 0;
   
}
</style>