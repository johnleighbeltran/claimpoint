<script setup>
import { ref } from 'vue'

const theme = ref('light')

function onClick() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
  <v-responsive class="border rounded">
    <v-app :theme="theme">
      <v-app-bar class="px-3" color="grey-lighten-1">
        <v-spacer></v-spacer>

        <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          text="Toggle Theme"
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main class="bg-amber-lighten-5">
        <v-container>
          <v-row>
            <v-col cols="12" md="6" class="mx-auto pt-16">
              <v-card
                class="mx-auto"
                color="orange-lighten-4"
                elevation="2"
              >
                <template v-slot:title>
                  <v-img src="/images/logofav.png" height="200"></v-img>
                </template>

                <v-card-text class="bg-orange-lighten-5 pt-4">
                  <v-form fast-fail @submit.prevent>
                    <v-text-field label="Firstname"></v-text-field>
                    <v-text-field label="Lastname"></v-text-field>

                    <v-text-field label="Email"></v-text-field>

                    <v-text-field label="Password" type="password"></v-text-field>
                    <v-text-field label="Password Confirmation" type="password"></v-text-field>

                    <v-btn class="mt-2" variant="tonal" type="submit" block>Submit</v-btn>
                  </v-form>
                  <v-divider class="my-5"></v-divider>

                  <h5 class="text-center">
                    Already have account? <RouterLink to="/login">Click Here to Login</RouterLink>
                  </h5>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-main>

      <v-footer color="amber-lighten-5" border app>2025 - TrackBack</v-footer>
    </v-app>
  </v-responsive>
</template>
