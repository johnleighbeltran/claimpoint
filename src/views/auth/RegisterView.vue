<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row>
        <v-col cols="12" md="6" class="mx-auto pt-16">
          <v-card class="mx-auto" color="orange-lighten-4" elevation="2">
            <template v-slot:title>
              <v-img src="/images/logofav.png"></v-img>
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
    </template>
  </AppLayout>
</template>
