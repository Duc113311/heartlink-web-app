<template>
  <!-- header -->
  <div>
    <div class="flex justify-center">
      <img
        src="../assets/images/logo-app.png"
        width="100"
        height="100"
        alt=""
        srcset=""
      />
    </div>
    <div class="block text-center justify-center mt-3">
      <span>Warm Welcome</span><br />
      <span>We hope you have a sweet time here</span>
    </div>
  </div>
  <!-- Body -->
  <div class="h-30 w-full bg-slate-300 justify-center inline-grid p-10">
    <button
      class="p-2 bg-sky-500 text-cyan-50 rounded-sm"
      @click="onLoginGoogle()"
    >
      Login with Google
    </button>
    <button
      @click="onLoginFacebook()"
      class="mt-3 p-2 bg-sky-500 text-cyan-50 rounded-sm"
    >
      Login with Facebook
    </button>
    <button
      @click="onLoginPhoneNumber()"
      class="mt-3 p-2 bg-sky-500 text-cyan-50 rounded-sm"
    >
      Login with PhoneNumber
    </button>
  </div>
</template>

<script>
// @ is an alias to /src
import { signInWithPopup, GoogleAuthProvider, auth } from "../configs/firebase";
export default {
  name: "Login-auth",
  components: {},
  setup() {},

  methods: {
    /**
     * Login Google
     */
    onLoginGoogle() {
      debugger;
      console.log("Da vào day");
    },

    /**
     * Login facebook
     */
    onLoginFacebook() {
      debugger;
    },

    /**
     * Login Phone Number
     */
    onLoginPhoneNumber() {
      debugger;
    },
  },
};
</script>
