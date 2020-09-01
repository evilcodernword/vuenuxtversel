<template>
  <div class="page-content d-flex justify-content-center mt-5 mb-5 ">
    <div class="sign-content mt-4">
      <div class="container">
        <div class="row register-part" v-if="!haveanaccount">
          <div class="form-left col-12 col-xl-6 col-md-6">
            <h2>INFOMATION</h2>
            <p class="text-1">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Et
              molestie ac feugiat sed. Diam volutpat commodo.
            </p>
            <p class="text-2">
              <span>Eu ultrices:</span> Vitae auctor eu augue ut. Malesuada nunc
              vel risus commodo viverra. Praesent elementum facilisis leo vel.
            </p>
            <div class="form-left-last">
              <button class="account" @click="togglehaveanaccount">Have An Account</button>
            </div>
          </div>
          <form
            class="form-detail col-12 col-xl-6 col-md-6"
            action="#"
            method="post"
            id="myform"
          >
            <h2>REGISTER FORM</h2>
            <div class="form-group">
              <div class="form-row form-row-1">
                <label for="first_name">First Name</label>
                <input
                  type="text"
                  name="first_name"
                  id="first_name"
                  class="input-text"
                />
              </div>
              <div class="form-row form-row-1">
                <label for="last_name">Last Name</label>
                <input
                  type="text"
                  name="last_name"
                  id="last_name"
                  class="input-text"
                />
              </div>
            </div>
            <div class="form-row">
              <label for="user_name">User Name</label>
              <input
                type="text"
                name="user_name"
                id="user_name"
                class="input-text"
              />
            </div>
            <div class="form-row">
              <label for="your_email">Your Email</label>
              <input
                type="text"
                name="your_email"
                id="your_email"
                class="input-text"
                required
                pattern="[^@]+@[^@]+.[a-zA-Z]{2,6}"
              />
            </div>
            <div class="form-group">
              <div class="form-row form-row-1 ">
                <label for="password">Password</label>
                <input
                  type="password"
                  name="password"
                  id="password"
                  class="input-text"
                  required
                />
              </div>
              <div class="form-row form-row-1">
                <label for="comfirm-password">Comfirm Password</label>
                <input
                  type="password"
                  name="comfirm_password"
                  id="comfirm_password"
                  class="input-text"
                  required
                />
              </div>
            </div>
            <div class="form-checkbox ">
              <div class="form-row">
                <input type="checkbox" id="terms" />
                <label for="terms"
                  ><p>
                    I agree to the
                    <a href="#" class="text">Terms and Conditions</a>
                  </p>
                </label>
              </div>
            </div>
            <div class="form-row-last">
              <input
                type="submit"
                name="register"
                class="register p-2"
                value="Register"
              />
            </div>
          </form>
        </div>
        <div class="row login-part" v-else>
          <div class="form-left col-12 col-xl-6 col-md-6">
            <h2>INFOMATION</h2>
            <p class="text-1">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Et
              molestie ac feugiat sed. Diam volutpat commodo.
            </p>
            <p class="text-2">
              <span>Eu ultrices:</span> Vitae auctor eu augue ut. Malesuada nunc
              vel risus commodo viverra. Praesent elementum facilisis leo vel.
            </p>
            <div class="form-left-last">
              <button class="account" @click="togglehaveanaccount">Create An Account</button>
            </div>
          </div>
          <form
            class="form-detail col-12 col-xl-6 col-md-6"
            action="#"
            method="post"
            id="myform"
          >
            <h2>Login Form</h2>
            <div class="form-row">
              <label for="your_email-login">Your Email</label>
              <input
                type="text"
                name="your_email-login"
                id="your_email"
                class="input-text"
                required
                pattern="[^@]+@[^@]+.[a-zA-Z]{2,6}"
              />
            </div>
            <div class="form-row">
              <label for="password-login">Password</label>
              <input
                type="password"
                name="password-login"
                id="password"
                class="input-text"
                required
              />
            </div>
            <div class="form-row-last">
              <input
                type="submit"
                name="Login"
                class="register p-2"
                value="Login"
              />
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
        haveanaccount:false,
    };
  },
  methods:{
      togglehaveanaccount(){
          this.haveanaccount=!this.haveanaccount
      }
  }
};
</script>

<style></style>
