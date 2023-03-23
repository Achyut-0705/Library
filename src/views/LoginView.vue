<template>
  <div class="center">
    <v-row>
      <v-col cols="10" offset="1">
        <!-- <h1>Login Page</h1> -->
        <v-avatar color="primary" size="128">
          <v-img src="@/assets/logo.jpg"></v-img>
        </v-avatar>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="10" offset="1">
        <h2>Sign in to your account</h2>
      </v-col>
    </v-row>
    <v-col cols="10" offset="1">
      <v-form v-model="valid" @submit.prevent="login($event)">
        <v-text-field
          v-model="email"
          :rules="emailRules"
          label="Email"
          required
          autofocus
        ></v-text-field>

        <v-text-field
          v-model="password"
          :rules="passwordRules"
          label="Password"
          type="password"
          required
        ></v-text-field>

        <v-btn color="primary" type="submit">Login</v-btn>
      </v-form>
    </v-col>
  </div>
</template>

<script>
export default {
  data() {
    return {
      valid: false,
      email: "",
      emailRules: [
        (v) => !!v || "E-mail is required",
        (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
      ],
      password: "",
      passwordRules: [
        (v) => !!v || "Password is required",
        (v) => v.length >= 8 || "Password must be at least 8 characters",
      ],
    };
  },
  methods: {
    login(event) {
      console.log("login");
    },
  },
};
</script>

<style lang="scss" scoped></style>
