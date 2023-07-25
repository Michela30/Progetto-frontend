<script>
//import

   export default {
    data() {
      return{
        //dati
       
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
        title: String,
        color: String,
        icon: String,
        colorHover: String
    
    }
    
    
  }
</script>


<template>

    <button :style="colorHover" :class="color" class="border rounded-pill">
        <i :class="icon">
           
        </i>
        {{ title }}
    </button>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

button{
    padding: 4px 18px;
}

</style>