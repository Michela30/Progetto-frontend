<script>
//import
import FirstSectionMain from './FirstSectionMain.vue'
import SecondSectionMain from './SecondSectionMain.vue'
import ThirdSectionMain from './ThirdSectionMain.vue'



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
        FirstSectionMain,
        SecondSectionMain,
        ThirdSectionMain,

    },
    props:{
        //utilizzo per file padre
    }
    
    
  }
</script>


<template>

    <main>
        <!-- first section -->
        
        <FirstSectionMain />

        <!-- Second section -->
    
        <SecondSectionMain />

        <!-- Second section -->

        <ThirdSectionMain />


    </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

</style>