<template>
  <div>
    <v-container>
      <v-row>
        <v-col md="6">
          <v-card tile elevation="0" >
            <h2 class="text-center pt-3" style="font-family: Playfair Display, serif; color: #0285b9">Welcome</h2>
            <v-card-text class="text-center" style="font-family: Playfair Display, serif; color: #0285b9; font-size: 18px;">
              Please Sign Up To Continue</v-card-text
            >
            <v-container>
              <v-row >
                <v-text-field
                  outlined
                  class="mx-6 my-2"
                  label="First Name"
                ></v-text-field>
                <v-text-field
                  outlined
                  class="mx-6 my-2"
                  label="Last Name"
                ></v-text-field>
              </v-row>
              <v-text-field
                outlined
                class="mx-3"
                label="E-mail Address"
              ></v-text-field>
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
              <v-text-field
                v-model="password"
                :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
                :rules="[rules.required, rules.min]"
                :type="show2 ? 'text' : 'password'"
                name="input-10-1"
                outlined
                class="mx-3"
                label="Confirm Password"
              ></v-text-field>
              <div class="text-center">
                <v-btn color="#0285b9" class="white--text mb-5" width="15em">
                  Sign Up</v-btn
                >
              </div>
            </v-container>
          </v-card>
        </v-col>
        <v-col md="6">
          <v-container>
            <v-img src="sign.jpg"></v-img>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
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
