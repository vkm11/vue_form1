<template>
    <div>
        <div v-if="error.length">
            <h3>Please correct the following errors</h3>
            <ul>
                <li v-for="e in error" v-bind:key="e.id">
                {{e}}
                </li>
            </ul>
        </div>
        <form @submit="login">
            <input type="text" placeholder="Enter name" v-model="name"/> <br> <br>
            <input type="password" placeholder="Enter password" v-model="password"/><br> <br>
            <button type="submit">Login</button>
        </form>
    </div>
</template>
<script>

export default {
   name: "Login-validation",
   data(){
       return{ 
           error:[],
           name:null,
           password:null,
       }
   },
   methods: { 
       login(e){
           this.error=[];
           if(this.name && this.password)
           {
               console.log("no error");
              
           }
           if(!this.name){
               this.error.push("user name is required");
           }
             if(!this.password){
               this.error.push("password is required");
           }
           console.log("Hello",this.error);
           e.preventDefault();
       }
   }
}
</script>