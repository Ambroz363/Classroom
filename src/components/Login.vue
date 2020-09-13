<template>
    
         <div class="login">
            <h1>LogIn</h1>
            <form @submit.prevent="pass">
            <p>E-mail</p>
            <input type="email" v-model="eml" name="Email" placeholder="Email" />
            <p>Password</p>
            <input type="password" v-model="pw" name="Password" placeholder="Password" />
            <p1>
                <a href="#">Forgot your password?</a>
            </p1>
            <input type="submit" value="Submit" >
            <p>Dont have an account yet?</p> 
            <p><a href="#" type="text">Sign up Now</a></p>   
            </form>
        </div>
    
</template>

<script>
export default {
    name:"Login",
    data() {
        return{
            eml:'',
            pw:''

        }
    },
    methods: {
        pass() {
            const lgin ={
                eml:this.eml,
                pw:this.pw
            }
            this.$emit("login-in",lgin)
        }
    }
    
}
</script>

<style scoped>
  .login{
    width: 1000px;
    height: 550px;
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
    padding: 65px 0 0px;
    position: relative;
    left: 650px;
    border: #707070;
    font-weight: bold;
}
p{
    color: black;
    position: relative;
    left: 650px;
    font-size: 15px;
    font-weight: bold;
    
    
}
p1{
    color: black;
    position: relative;
    left: 650px;
    font-size: 15px;
    font-weight: bold;
    
}
.login input[type="email"]
{
    margin: 0px 650px 0px;
    padding: 5px 5px 5px;
    background: rgb(235, 252, 249);
    
    font-size: small;
    border: none;
    border-bottom-style: groove;
}
.login input[type="password"]
{
    margin: 0px 650px 10px;
    padding: 5px 5px 5px;
    
    background: rgb(235, 252, 249);
    font-size: small;
    border: none;
    border-bottom-style: groove;
}
.login input[type="submit"]
{
    margin: 5px 650px 10px;
    padding: 5px 70px 5px;
    font-size: 16px;
    border: none;
    border-radius: 15px 15px 15px;
    background: #9C39E4;
    color: white;
}      


</style>

// Adadasda