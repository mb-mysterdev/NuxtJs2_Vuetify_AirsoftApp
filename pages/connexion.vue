<template>
  <v-app>
    <v-dialog v-model="dialog" max-width="600px" min-width="360px" persistent>
      <div>
        <v-tabs
          v-model="tab"
          background-color="deep-purple accent-4"
          dark
          grow
          icons-and-text
          show-arrows
        >
          <v-tabs-slider color="purple darken-4" />
          <v-tab v-for="i in tabs" :key="i">
            <v-icon large>
              {{ i.icon }}
            </v-icon>
            <div class="caption py-1">
              {{ i.name }}
            </div>
          </v-tab>
          <v-tab-item>
            <v-card class="px-4">
              <v-card-text>
                <v-form ref="loginForm" lazy-validation>
                  <v-row>
                    <v-col cols="12">
                      <v-text-field
                        v-model="loginEmail"
                        label="E-mail"
                        required
                      />
                    </v-col>
                    <v-col cols="12">
                      <v-text-field
                        v-model="loginPassword"
                        :append-icon="show1?'eye':'eye-off'"
                        :type="show1 ? 'text' : 'password'"
                        counter
                        hint="At least 8 characters"
                        label="Password"
                        name="input-10-1"
                        @click:append="show1 = !show1"
                      />
                    </v-col>
                    <v-col class="d-flex" cols="12" sm="6" xsm="12" />
                    <v-spacer />
                    <v-col align-end class="d-flex" cols="12" sm="3" xsm="12">
                      <v-btn block color="success" x-large @click="validate">
                        Login
                      </v-btn>
                    </v-col>
                  </v-row>
                </v-form>
              </v-card-text>
            </v-card>
          </v-tab-item>
          <v-tab-item>
            <v-card class="px-4">
              <!--              <v-card-text>-->
              <!--                <v-form ref="registerForm" v-model="valid" lazy-validation>-->
              <!--                  <v-row>-->
              <!--                    <v-col cols="12" md="6" sm="6">-->
              <!--                      <v-text-field-->
              <!--                        v-model="firstName"-->
              <!--                        :rules="[rules.required]"-->
              <!--                        label="First Name"-->
              <!--                        maxlength="20"-->
              <!--                        required-->
              <!--                      />-->
              <!--                    </v-col>-->
              <!--                    <v-col cols="12" md="6" sm="6">-->
              <!--                      <v-text-field-->
              <!--                        v-model="lastName"-->
              <!--                        :rules="[rules.required]"-->
              <!--                        label="Last Name"-->
              <!--                        maxlength="20"-->
              <!--                        required-->
              <!--                      />-->
              <!--                    </v-col>-->
              <!--                    <v-col cols="12">-->
              <!--                      <v-text-field v-model="email" :rules="emailRules" label="E-mail" required />-->
              <!--                    </v-col>-->
              <!--                    <v-col cols="12">-->
              <!--                      <v-text-field-->
              <!--                        v-model="password"-->
              <!--                        :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"-->
              <!--                        :rules="[rules.required, rules.min]"-->
              <!--                        :type="show1 ? 'text' : 'password'"-->
              <!--                        counter-->
              <!--                        hint="At least 8 characters"-->
              <!--                        label="Password"-->
              <!--                        name="input-10-1"-->
              <!--                        @click:append="show1 = !show1"-->
              <!--                      />-->
              <!--                    </v-col>-->
              <!--                    <v-col cols="12">-->
              <!--                      <v-text-field-->
              <!--                        v-model="verify"-->
              <!--                        :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"-->
              <!--                        :rules="[rules.required, passwordMatch]"-->
              <!--                        :type="show1 ? 'text' : 'password'"-->
              <!--                        block-->
              <!--                        counter-->
              <!--                        label="Confirm Password"-->
              <!--                        name="input-10-1"-->
              <!--                        @click:append="show1 = !show1"-->
              <!--                      />-->
              <!--                    </v-col>-->
              <!--                    <v-spacer />-->
              <!--                    <v-col class="d-flex ml-auto" cols="12" sm="3" xsm="12">-->
              <!--                      <v-btn :disabled="!valid" block color="success" x-large @click="validate">-->
              <!--                        Register-->
              <!--                      </v-btn>-->
              <!--                    </v-col>-->
              <!--                  </v-row>-->
              <!--                </v-form>-->
              <!--              </v-card-text>-->
            </v-card>
          </v-tab-item>
        </v-tabs>
      </div>
    </v-dialog>
  </v-app>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Login',
  layout: 'empty',
  data: () => ({
    dialog: true,
    tab: 0,
    tabs: [
      {
        name: 'Login',
        icon: 'mdi-account'
      },
      {
        name: 'Register',
        icon: 'mdi-account-outline'
      }
    ],

    loginPassword: '',
    loginEmail: '',
    show1: false
  }),
  methods: {
    validate () {
      axios.post('http://localhost:8000/api/login', {
        email: this.loginEmail,
        password: this.loginPassword
      }).then((res) => {
        console.log(res)
      })
    }
  }
}
</script>

<style scoped>

</style>
