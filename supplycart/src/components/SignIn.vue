<template>
<div class="container ">
    <div class="flex h-full justify-center items-center ">
      <div class="box h-4/5 bg-gray-200 bg-opacity-90 w-5/12 rounded-lg shadow-lg">
        <div class="wrapper w-4/5">
            <h2 class="text-3xl font-serif">Welcome back</h2>
            <div class="input-area">
                <h3>Email</h3> 
                <input class="textbox rounded-lg bg-gray-100" type="email" placeholder="Email" height="20" width="50">
                <br>
                <br>
                <h3>Password</h3>
                <input class="textbox rounded-lg bg-gray-100" type="password" placeholder="Password" height="20" width="50">
            </div>
            <button class="mt-8 bg-gray-50 rounded-lg shadow-lg px-4 py-1 hover:bg-gray-300" @click="goToMain()">Sign In</button>
            <br>
            <br>
            <router-link to="/signup" class="underline text-blue-600">Create new account</router-link>
        </div>
      </div>
      
  </div>
</div>
</template>

<script>
export default {
    name: "SignIn",
    methods: {
        goToMain(){
            this.$router.push({name:'Main'})
            console.log("signin success")
        }
    }
}

</script>

<style scoped>
.wrapper {
    text-align: center;
    margin: 10% auto;
    padding: 20px;
}

.input-area {
    text-align: left;
    margin-top: 30px;
    padding: 0px 20px;
}

.textbox {
    margin-top: 5px;
    height: 8vh;
    width: 100%;
}

.container {
    background: url('../assets/signin-page-bg.jpg');
    background-size: 100% 180%;
    background-position: bottom left;
    padding-top: 20px;
    padding-bottom: 90px;
}

@media screen and (max-width: 800px) {
    .box{
        width:75%;
    }
}
</style>