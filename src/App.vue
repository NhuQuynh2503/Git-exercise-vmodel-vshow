<template>
      <div id="login-container">
            <h2>Log in</h2>
            <span>to start learning</span>
          <form action="">
            <div class="form-group">
              <label for="twitter">Twitter handle</label>
              <input v-model="twitter" type="email" name="twitter" id="twitter" required>
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input v-model="password" type="password" name="password" id="password" required>
            </div>
            <a href="">Forgot password?</a>
            <button class="btn" @click="change">
            <p >Log in</p> 
            <Icon class="i" icon="basil:arrow-right-outline"></Icon></button>
          </form>
          <p class="submit" v-show="showSuccess">{{ successMessenger }}</p>
      </div>
</template>
<script setup>
  import {ref} from "vue"
  const twitter = ref('')
  const password = ref('')
  const showSuccess =  ref(false)
  const successMessenger = ref('')
  function change(value){
    twitter.value=''
    password.value=''
    showSuccess.value=true
    successMessenger.value='Thanh cong!'
    
  }
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
body {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-style: italic;
  background-color: #f0f0f0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  
} 
#login-container{
  width: 20rem;
  height: 27rem;
  border: .1rem solid rgba(0, 0, 0, .1);
  border-radius: 2rem;
  margin: 9rem auto;
}
h2{
  font-size: 2rem;
  margin-left: 1rem;
}
span{
  font-size: 1.2rem;
  margin-left: 1rem;
  color: #343434;
}
form{
  padding-top: 1rem;
  margin: 0 1rem;
  width: 20rem;
}
form .form-group{
  margin-bottom: 15px;
}
form .form-group label{
  display: block;
  padding-bottom: .5rem;
  color: #BEBEBE;
}
form .form-group input{
  width: 17.3rem;
  height: 1.5rem;
}
a{
  color: #BEBEBE;
  text-decoration: none;
  display: block;
  padding-bottom: 1.5rem;
}
.btn{
  /* padding:0 6.3rem; */
  height: 3rem;
  width: 17.7rem;
  background: #0C6CDA;
  border: none;
  font-size: 1rem;
  border-radius: .3rem;
  color: #E4EFFB;
  display: flex;
  /* text-align: center; */
  justify-content: center;
  
}
.btn p{
  font-size: 1.2rem;
  margin:.8rem 0;
  /* padding-bottom: 4rem; */
}
.btn .i{
  padding-top: .5rem;
  font-size: 2rem;
  color: #E4EFFB;
}
.submit{
  font-size: 1.2rem;
  color: #E23C3C;
  text-align: center;
}
</style>