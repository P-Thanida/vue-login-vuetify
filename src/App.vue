<template>
  <v-app>
    <v-app-bar app dark color="red">
      <v-toolbar-title>Login</v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- ขอบมน -->
      <!-- <v-btn text rounded>Home</v-btn> -->

      <!-- ขอบเหลี่ยม -->
      <v-btn text>Home</v-btn>
      <v-btn text>Login</v-btn>
      <v-btn text>About</v-btn>
      <v-btn text>Contact us</v-btn>
    </v-app-bar>
    <v-content>
      <!-- mx=ตรงกลาง mt=ห่างจากขอบบน -->
      <v-card width="450" class="mx-auto mt-9">
        <v-card-title> Login </v-card-title>
        <v-card-text>
          <v-text-field label="Username" prepend-icon="mdi-account-circle" />
          <v-text-field
            label="Password"
            :type="showPassword ? 'text' : 'password'"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn app dark color="red">Login</v-btn>
          <v-btn app dark color="red">Register</v-btn>
        </v-card-actions>
      </v-card>
    </v-content>
    <template>
      <v-footer dark padless>
        <v-card class="flex" app dark color="red" flat tile>
          

          <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </template>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>
