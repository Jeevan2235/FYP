<template>
  <div>
    <v-row>
      <v-col md="6" class="pa-10">
        <v-card-text style="font-family: Playfair Display, serif; font-size: 20px; color: #0285b9;">Email Address</v-card-text>
        <v-text-field
          outlined
          class="mx-3"
          label="E-mail Address"
        ></v-text-field>
         <v-card-text style="font-family: Playfair Display, serif; font-size: 20px; color: #0285b9;">Password</v-card-text>
        <v-text-field
          outlined
          class="mx-3"
          label="Password"
          v-model="password"
          :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
          :rules="[rules.required, rules.min]"
          :type="show1 ? 'text' : 'password'"
          name="input-10-1"
          @click:append="show1 = !show1"
        ></v-text-field>
        <div class="text-center">
          <v-btn
            class="mb-5  white--text"
            width="17em"
            color="#0596c8"
            height="3.5em"
            >LogIn</v-btn
          >
        </div>
      </v-col>

      <v-col md="6">
        <v-container>
          <v-img src="login.png"  ></v-img>
        </v-container>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show1: false,
      show2: true,
      show3: false,
      show4: false,
      password: "Password",
      rules: {
        required: (value) => !!value || "Required.",
        min: (v) => v.length >= 8 || "Min 8 characters",
        emailMatch: () => `The email and password you entered don't match`,
      },
    };
  },
};
</script>

<style></style>
