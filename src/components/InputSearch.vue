<script>
//import

   export default {
    data() {
      return{
        //dati
        categoriesValue: '',
        //array delle categorie
      }
    },
    methods: {
        //function
       searchCategories(){
            if(this.categoriesValue == id categoria){
                return la categoria
            }
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

<form action="">
    <div class="input-group">
        <input type="text" class=" rounded-pill border border-none ps-2 w-100" placeholder="Search..." aria-label="Search" aria-describedby="button-addon2">

        <button class="btn rounded-circle send-button" type="submit" id="button-addon2">
            <i class="fa-xs fa-solid fa-magnifying-glass"></i>
        </button>
    </div>
</form>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

form{
    margin-left: 35px;

    input{
        height: 40px;
        font-size: 0.6em;
        position: relative;
    }

    .send-button{
        background-color: $color-yellow;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        position: absolute;
        right: -10px;
        color: white;
        box-shadow: -20px -1px 31px -11px #F7F8FA;
    }
}
</style>