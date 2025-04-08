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
            <slot name=""></slot>
        </v-container>
      </v-main>

      <v-footer color="amber-lighten-5" border app>2025 - LostnFound</v-footer>
    </v-app>
  </v-responsive>
</template>
