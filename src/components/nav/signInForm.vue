<template>
  <div class="sign-in-form">
    <div class="bg">
      <form @submit.prevent="onSubmit">
        <p>Sign In</p>
        <input
          v-model="Fname"
          type="text"
          placeholder="First Name"
          name="name"
          required
        />
        <input
          v-model="Lname"
          type="text"
          placeholder="Last Name"
          name="name"
          required
        />

        <select v-model="gender">
          <option value="" disabled="" selected="selected" >Choose A Title</option>
          <option value="0">Mr</option>
          <option value="1">Ms</option>
        </select>

        <button class="login" type="submit" @click="submit">Submit</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignInForm",
  data() {
    return {
      Fname: "",
      Lname: "",

      gender: "Choose a Title",
    };
  },
  methods: {
    submit() {
      if (this.Lname && this.Fname && this.gender) {
        let info = {
          loggedIn: true,
          name: this.name,
          gender: this.gender,
        };
        this.$emit("info-submitted", info);
        (this.name = ""), (this.gender = "");
      }
    },
  },
  computed: {
    name() {
      return this.Fname + " " + this.Lname;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/_utilities";
.login {
  @include button;
  color: white;
  transition: 0.2s all ease-out;
  background-color: $blue;

  &:hover {
    background-color: white;
    color: $blue;
  }
}
.sign-in-form {
  position: fixed;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  z-index: 5;
  overflow: hidden;
}
.bg {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.671);
  color: white;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

form {
  width: 400px;
  background-color: white;
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  p {
    font-size: 30px;
    color: $blue;
    margin-bottom: 15px;
  }
}
select {
  margin: 15px 0;
}
input {
  border: none;
  border-bottom: 2px solid $blue;
  outline: none;
  text-align: center;
  margin: 10px 0;
}
</style>
