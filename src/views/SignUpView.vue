<template>
  <div class="container">
    <h1>this is the Signup page</h1>
    <div class="formContainer">
      <div class="formWrapper">
        <span class="logo">layttCreations</span>
        <span class="title">{{ title }}</span>
        <form class="Signup" @submit.prevent="Signup">
          <label>FirstName</label>
          <input
            type="text"
            v-modal="firstName"
            placeholder="First Name"
            required
          />
          <label>LastName</label>
          <input
            type="text"
            v-modal="lastName"
            placeholder="Last Name"
            required
          />
          <label>PhoneNumber</label>
          <input
            type="phoneNumber"
            v-modal="phoneNumber"
            placeholder="Phone Number"
            required
          />
          <label>Email</label>
          <input type="email" v-modal="email" placeholder="Email" required />
          <label>Password</label>
          <input
            type="password"
            v-modal="password"
            placeholder="password"
            required
          />
          <label for="ConfirmPassword">
            <input type="password" placeholder="Re-type password" v-modal="password" required
          /></label>
          
<!--<label for="checkbox">
            <input type="checkbox" id="checkbox" />
            <span> I agree to the terms and conditions</span>
          </label>  -->
          <button @click="signUp">Signup</button>
        </form>
        <p>
        Already have an account?
        <router-link :to="{ name: login }"><button>login</button></router-link>
      </p>
        
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "SignUp",
      firstName: "",
      lastName: "",
      phoneNumber: "",
      email: "",
      password: "",
    };
  },
  methods: {
    signUp() {
      console.log("signing up");
      this.$store.dispatch("auth/signup", {
        firstName: this.firstName,
        lastName: this.lastName,
        phoneNumber: this.phoneNumber,
        email: this.email,
        password: this.password,
      });
    },
  },
};
</script>

<style scoped>
.container {
  background-color: rgb(156, 156, 216);
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.formContainer {
  background-color: rgb(156, 156, 216);
  height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.formWrapper {
  padding: 10px 30px;
  height: 90%;
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

.Signup {
  display: flex;
  flex-direction: column;
  gap: 10px;
  height: 80%;
}

input {
  padding: 15px;
  border: none;
  border-bottom: 1px solid rgb(228, 198, 248);
  width: 250px;
}

::placeholder {
  color: rgba(201, 196, 196, 0.651);
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
  font-weight: bold;
  align-items: center;
  color: rgb(25, 2, 233);
  font-size: 12px;
  gap: 8px;
  align-items: center;
  cursor: pointer;
}

p {
  font-size: 14px;
  margin-top: 0.5em;
  color: rgb(189, 140, 140);
}
</style>
