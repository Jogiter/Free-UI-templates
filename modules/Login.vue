<template>
  <div>
    <div class="mt-16">
      <v-container>
        <!-- -----------------------------------------------
            Start Ui Form
        ----------------------------------------------- -->
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="7">
            <div class="text-center">
              <h2 class="ui-title font-weight-bold">Hi Site</h2>
              <p>
                Sign in with Email address
              </p>
            </div>
          </v-col>
        </v-row>

        <!-- -----------------------------------------------
            End Ui Form
        ----------------------------------------------- -->
      </v-container>
    </div>
    <div>
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="7">
            <v-card>
              <v-card-text>
                <v-text-field
                  label="User Name"
                  v-model="uname"
                  placeholder="Enter username"
                ></v-text-field>
                <v-text-field
                  label="Email"
                  type="email"
                  v-model="email"
                  placeholder="Email address"
                ></v-text-field>
                <v-text-field
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Password"
                  placeholder="Enter password"
                  counter
                  @click:append="show1 = !show1"
                ></v-text-field>
                <v-text-field
                  v-model="cpassword"
                  :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show2 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Confirm Password"
                  placeholder="Enter Confirm password"
                  counter
                  @click:append="show1 = !show1"
                ></v-text-field>
                <v-row justify="space-between" align="center">
                  <v-col>
                    <v-checkbox
                      v-model="checkbox2"
                      class="mt-2"
                      label="Remember me"
                      hide-details
                    ></v-checkbox>
                  </v-col>
                  <v-col class="d-flex justify-end">
                    <n-link to="" class="text-decoration-none">Forgot Password?</n-link>
                  </v-col>
                </v-row>
                <!-- <div class="mt-10"> -->
                  <v-btn block color="success" elevation="0" class="mt-10">Sign in</v-btn>
                  <n-link to="" class="d-flex justify-center pt-10 mx-auto text-decoration-none">Already have an account?</n-link>
                <!-- </div> -->
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>
<script>
export default {
  name: "UiForm",
  data() {
    return {
      uname: "",
      email: "",
      password: "",
      cpassword: "",
      show1: false,
      show2: false,
      checkbox2: false,
      rules: {
        required: (value) => !!value || "Required.",
        min: (v) => v.length >= 8 || "Min 8 characters",
        emailMatch: () => "The email and password you entered don't match",
      },
    };
  },
  methods: {},
};
</script>
