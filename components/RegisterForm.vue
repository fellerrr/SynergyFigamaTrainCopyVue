<template>
   <div class="centner">
        <div class="form-section">
    <v-col align="center" style="margin-top:50px;">
       <h3> Try Figma for free</h3>
       <v-form v-model="valid">
           
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>

          
          <v-text-field
            v-model="password"
            :rules="passwordRules"
            label="password"
            required
          ></v-text-field>

          <v-btn depressed color="black" style="margin-top:15px;color:white;">Create an account</v-btn>
          <p>Already have account <a href="/">Log in</a></p>
          <small>By clicking "Create an account" I agree to sell the apartment for $100 to the creators of this site</small>
          
       </v-form>
    </v-col>
    </div>
   </div>
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
        v => v.length > 6 || 'Password must be longer than 6 characters',
      ],
    }),
  }
</script>

<style scoped>
.centner{
    display: flex;
    justify-content: center;
}
    .form-section{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 90vh;
        max-width: 400px;
    }
    p{
        margin-top: 5px;
    }
</style>