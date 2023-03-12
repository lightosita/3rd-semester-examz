<template>
  <div class='container'>
    <h1>this is the login page</h1>
    <div class="formContainer">
        <div class="formWrapper">
          <span class="logo">layttCreations</span>
          <span class="title">Login</span>
          <form class="login" @submit.prevent="login">
           <label for="email">
            <input type="email"
             v-modal="email" 
             placeholder="email"
             autocomplete="on" />
           </label>
            
           <label for="password">
            <input type="password" v-modal="email"  placeholder="password" />
           </label>
            <button type="submit">Login</button>
          </form>
          <p>Don't have an account? Register!!</p>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "loginIn",
      email:"",
      password:"",
    };
  },
  methods: {
    login() {
      console.log("logedIn")
    }
  } 
};
</script>

<style scoped>
.formContainer {
  background-color: rgb(156, 156, 216);
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;

}

  .formWrapper {
    padding: 20px 60px;
    background-color: white;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    align-items: center;
  }

.logo {
      color: rgb(130, 82, 161);
      font-weight: bold;
      font-size: 24px;
    }
.title {
      color: rgb(130, 82, 161);
      font-size: 12px;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

input {
        padding: 15px;
        border: none;
        border-bottom: 1px solid rgb(228, 198, 248);
        width: 250px;
}

::placeholder {
          color: grey;
        }


 button {
        background-color: rgb(128, 76, 128);
        padding: 10px;
        font-weight: bold;
        border-radius: 5px;
        color: white;
        border: none;
        cursor: pointer;
      }

      label {
        display: flex;
        align-items: center;
        color: rgb(71, 178, 184);
        font-size: 12px;
        gap: 10px;
        align-items: center;
        cursor: pointer;
      }

        

    p {
      font-size: 14px;
      margin-top: 10px;
      color: grey;
    }
 

  
</style>
