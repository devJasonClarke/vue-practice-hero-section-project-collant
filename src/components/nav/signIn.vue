<template>
  <div>
    <a v-if="!loggedIn" href="#" class="login" @click="signInForm"
      >Sign In</a
    >
    <div v-if="loggedIn" @click="signIn" class="login logged-in">
      <img :src="gender[selectGender]" alt="" srcset="" class="gen-icon" />
      {{ name }}
    </div>
  </div>
  <SignInForm v-if="form" @info-submitted="addUser" />
 
</template>

<script>
import man from "../../assets/images/man.svg";
import woman from "../../assets/images/woman.svg";
import SignInForm from "./signInForm";
export default {
  name: "SignIn",
  components: {
    SignInForm,
  },
  data() {
    return {
      loggedIn: false,
      name: "",
      gender: [man, woman],
      form: false,
      info: [],
      selectGender: "",
    };
  },
  methods: {
    signIn() {
      this.loggedIn = !this.loggedIn;
    },
    signInForm() {
      this.form = true;
    },
    addUser(info) {
      this.info.push(info);
      this.loggedIn = this.info[0].loggedIn;
      this.name = this.info[0].name;
      this.selectGender = this.info[0].gender;
      this.form = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/_utilities";
.login {
  @include button;
  color: $blue;
  transition: 0.2s all ease-out;
  &:hover {
    background-color: $blue;
    color: white;
  }
}
.logged-in {
  display: flex;
  align-items: center;
}
.gen-icon {
  height: 25px;
  margin-right: 15px;
}
</style>
