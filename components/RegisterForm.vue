<template>
    <v-row justify="center">
        <div class="form-section d-flex justify-center align-center">
            <v-col>
                    <h2>Try Figma for free</h2>

            <v-form v-model="value">

                <v-col align="center">

                    <v-text-field
                        v-model="email"
                        :rules="emailRules"
                        label="E-mail"
                        required
                    ></v-text-field>

                    <v-text-field
                        v-model="password"
                        :rules="passwordRules"
                        label="Password"
                        required
                    ></v-text-field>

                    <v-btn outlined color="black" style="margin: 10px 0;">
                            Create account
                        </v-btn>
                </v-col>

                    <p align="center"> Already have an account? <a href="">Log in</a> </p>
                    <small>By clicking "Create account", I agree to Figma's TOS and Privacy Policy.</small>

            

            </v-form>
            
                </v-col>
         </div>
    </v-row>
</template>


<script>
  export default {
    data: () => ({
      valid: false,
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],

      password: '',
      passwordRules: [
        v => !!v || 'Password is required',
        v => v.length > 6 || 'Password must not be less than 6 charae',
      ],
    }),
  }
</script>


<style scoped>
    .form-section{
        height: 95vh;
        max-width: 400px;
    }
</style>