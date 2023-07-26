<script>
//import

   export default {
    data() {
      return{
        //dati
       email: [],
       writeEmail: ''
      }
    },
    methods: {
        //function
        getEmail(){
            this.email.push(this.writeEmail)
            console.log(this.email)

            this.writeEmail = ''
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

   <section class="fourth-section">

    <!-- newsletter -->

       <div class="d-flex justify-content-center align-items-center">
            <h4 class="text-white">
                Subscribe Now to Our Newsletter!
            </h4>

            <form action="" method="get"  @submit.prevent="getEmail()">
                <div class="input-group">
                    <input v-model="writeEmail" type="email" class="rounded-pill border border-none ps-2" placeholder="Email address..." aria-label="Email address" required>

                    <button class="btn rounded-circle send-button" type="submit">
                        <i class="fa-xs fa-solid fa-paper-plane"></i>
                    </button>
                </div>
            </form>
       </div>
        
   </section>
   
</template>




<style lang="scss" scoped>
@use '../assets/scss/variables.scss' as *;

.fourth-section{
    background-color: $color-coral-primary;
    padding: 40px 0;

    h4{
        margin-right: 20px;
    }

    form{
        margin-left: 35px;

        input{
            width: 250px;
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
}
</style>