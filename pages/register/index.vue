<template>
  <div>
    <!-- Login Form -->
    <form @submit.prevent="submit">
      <input
        type="text"
        class="fadeIn second"
        placeholder="Nama"
        v-model="data.name"
      />
      <input
        type="email"
        class="fadeIn third"
        placeholder="Email"
        v-model="data.email"
      />
      <input
        type="text"
        class="fadeIn fourth"
        placeholder="Username"
        v-model="data.username"
      />
      <input
        type="text"
        class="fadeIn fourth password"
        placeholder="Password"
        v-model="data.password"
      />
      <input
        type="text"
        class="fadeIn fourth password"
        placeholder="Confirm Password"
        v-model="data.confirmpassword"
      />
      <input type="submit" class="fadeIn fourth" value="Register" />
    </form>
  </div>
</template>

<script>
import swal from 'sweetalert'
// import axios from 'axios'
export default {
  layout: 'login',
  auth: false,
  data() {
    return {
      data: {
        name: null,
        email: null,
        username: null,
        password: null,
        confirmpassword: null
      }
    }
  },
  methods: {
    async submit() {
      if (
        !this.data.name ||
        !this.data.email ||
        !this.data.username ||
        !this.data.password ||
        !this.data.confirmpassword
      ) {
        swal({
          text: 'Harap Lengkapi data!',
          icon: 'error',
          timer: 2000,
          button: false
        })
      }
      if (this.data.password == this.data.confirmpassword) {
        try {
          await this.$axios
            .post('https://ahlikasir-api.herokuapp.com/api/users', {
              name: this.data.name,
              email: this.data.email,
              username: this.data.username,
              password: this.data.password
            })
            .then((response) => {
              if (response.data.status == 'success') {
                swal({
                  icon: response.data.status,
                  text: response.data.message,
                  timer: 2000,
                  button: false
                })
              }

              swal({
                text: response.data.message,
                icon: response.data.status,
                timer: 2000,
                button: false
              })
            })

          await this.$auth.loginWith('local', {
            data: {
              username: this.data.username,
              password: this.data.password
            }
          })

          this.$router.push('/admin')
        } catch (error) {
          console.log(error)
        }
      } else {
        swal({
          text: 'Password Incorrect!',
          icon: 'error',
          button: 'Ouchhh'
        })
      }
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Poppins');

/* FORM TYPOGRAPHY*/

input[type='button'],
input[type='submit'],
input[type='reset'] {
  background-color: #56baed;
  border: none;
  color: white;
  padding: 15px 80px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  text-transform: uppercase;
  font-size: 13px;
  -webkit-box-shadow: 0 10px 30px 0 rgba(95, 186, 233, 0.4);
  box-shadow: 0 10px 30px 0 rgba(95, 186, 233, 0.4);
  -webkit-border-radius: 5px 5px 5px 5px;
  border-radius: 5px 5px 5px 5px;
  margin: 5px 20px 40px 20px;
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}

input[type='button']:hover,
input[type='submit']:hover,
input[type='reset']:hover {
  background-color: #39ace7;
}

input[type='button']:active,
input[type='submit']:active,
input[type='reset']:active {
  -moz-transform: scale(0.95);
  -webkit-transform: scale(0.95);
  -o-transform: scale(0.95);
  -ms-transform: scale(0.95);
  transform: scale(0.95);
}

input[type='text'],
input[type='email'] {
  background-color: #f6f6f6;
  border: none;
  color: #0d0d0d;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 5px;
  width: 85%;
  border: 2px solid #f6f6f6;
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  -ms-transition: all 0.5s ease-in-out;
  -o-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  -webkit-border-radius: 5px 5px 5px 5px;
  border-radius: 5px 5px 5px 5px;
}

input[type='text']:focus,
input[type='email']:focus {
  background-color: #fff;
  border-bottom: 2px solid #5fbae9;
}

input[type='text']:placeholder,
input[type='email'] {
  color: #cccccc;
}

/* ANIMATIONS */

/* Simple CSS3 Fade-in-down Animation */
.fadeInDown {
  -webkit-animation-name: fadeInDown;
  animation-name: fadeInDown;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}

@-webkit-keyframes fadeInDown {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -100%, 0);
    transform: translate3d(0, -100%, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, -100%, 0);
    transform: translate3d(0, -100%, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}

/* Simple CSS3 Fade-in Animation */
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fadeIn {
  opacity: 0;
  -webkit-animation: fadeIn ease-in 1;
  -moz-animation: fadeIn ease-in 1;
  animation: fadeIn ease-in 1;

  -webkit-animation-fill-mode: forwards;
  -moz-animation-fill-mode: forwards;
  animation-fill-mode: forwards;

  -webkit-animation-duration: 1s;
  -moz-animation-duration: 1s;
  animation-duration: 1s;
}

.fadeIn.first {
  -webkit-animation-delay: 0.4s;
  -moz-animation-delay: 0.4s;
  animation-delay: 0.4s;
}

.fadeIn.second {
  -webkit-animation-delay: 0.6s;
  -moz-animation-delay: 0.6s;
  animation-delay: 0.6s;
}

.fadeIn.third {
  -webkit-animation-delay: 0.8s;
  -moz-animation-delay: 0.8s;
  animation-delay: 0.8s;
}

.fadeIn.fourth {
  -webkit-animation-delay: 1s;
  -moz-animation-delay: 1s;
  animation-delay: 1s;
}

/* OTHERS */

*:focus {
  outline: none;
}

.password {
  -webkit-text-security: disc;
}
</style>
