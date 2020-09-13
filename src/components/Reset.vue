<template>
    <div class="resetbox">
        <form @submit.prevent="pass">
            <h1>Reset Password</h1>
            <div><p>New Password</p></div>
            <input type="password" v-model="pw1" name="Password" placeholder="Password">
            <div><p>Re-enter New Password</p></div>
            <input type="password" v-model="pw2" name="RePassword" placeholder="Password">
            <div>
                <input type="submit" value="Submit">
            </div>

        </form>
    </div>
</template>

<script>
export default {
   name: "Reset",
   data() {
       return {
           pw1:'',
           pw2:''
       }
   },
   methods: {
       pass() {
           const rein={
               pw1:this.pw1,
               pw2:this.pw2
           }

           this.$emit("reset-in",rein)
       }
   } 
}
</script>

<style scoped>
    .resetbox{
    width: 300px;
    height: 250px;
    background: white;
    color: #fff;
    top: 50%;
    left: 50%;
    position: absolute;
    transform: translate(-50%,-50%);
    box-sizing: border-box;
    border-radius: 15px 15px 15px;
    
}

h1{
    color: #393939;
    margin-top: 10px;
    padding: 0 0 0px;
    text-align: center;
    font-size: 22px;
    border: #707070;
}
p{
    color: grey;
    margin-bottom: 0px;
    
    
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: 12px;
    
}

.resetbox p{
    margin: 0;
    
    font-weight: bold;
    
    padding: 5px 30px 5px;

}



.resetbox input[type="password"]
{
    
    background: #F2F5FA;
    outline: none;
    width: 70%;
    height: 30px;
    margin-bottom: 10px;
    margin-left: 35px;
    border-radius: 5px 5px 5px;
    border-style: none;
    
}
.resetbox input[type="submit"]
{
    background: #9C39E4;
    color: whitesmoke;
    outline: none;
    border: none;
    align-items: center;
    margin: 8px 45px 0px;
    padding: 10px 10px 10px;
    width: 70%;
    border-radius: 15px 15px 15px;
    
}
</style>