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
    }
    
    
  }
</script>


<template>

    <button :class="color" class="rounded-pill">
        <i :class="icon">
           
        </i>
        {{ title }}
    </button>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

button{
    border: 1px solid transparent;
    padding: 10px 30px;
    font-size: 0.9em;
    font-weight: bolder;
}

//button component 1

.button-yellow{
    background-color: $color-yellow;
    color: white;
}
.header-top-button button{
    padding: 4px 18px;
}
.header-top-button button:hover{
    background-color: white;
    color: $color-coral-primary;
}

//button component 2

.buttonDue button{
    margin-left: 80px;
}
.buttonDue button:hover{
    background-color: $color-coral-primary;
    color: white;
}
//button component 3

.button-white{
    background-color: white;
    color: $color-coral-primary;
}

.buttonTre button:hover{
    background-color: $color-coral-secondary;
    color: white;
}

.buttonTre button{
    margin-right: 80px;
}

//button component 4

.buttonFour button{
    margin-left: 80px;
}
.buttonFour button:hover{
    background-color: $color-red;
    color: white;
}

//button component 5
.button-coral{
    color: white;
    background-color: $color-coral-primary;
}

.buttonFive button{
    
    margin-left: 80px;
}
.buttonFive button:hover{
    background-color: $color-yellow;
}

//button component 6

.buttonSix button{
    padding: 4px 18px;
    position: absolute;
    bottom: -10px;
    left: 65px;
    box-shadow: -1px 7px 15px -2px #000000;
}

//button component 7
.buttonSeven button{
    margin-top: 50px;
}

.buttonSeven button:hover{
    background-color: $color-coral-primary;
    color: white;
    box-shadow: -2px 4px 25px -12px #000000;
}

//button component 8
.buttonEight button{
    padding: 1px 10px;
    position: absolute;
    bottom: -10px;
    left: 40px;
}

//button component 9/10

.buttonNine button:hover{
    background-color: $color-yellow;
}

</style>