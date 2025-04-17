<script setup>
import { ref } from 'vue'


</script>

<template>
  <v-responsive class="border rounded">
    <v-app>
      <v-app-bar class="px-3" color="grey-lighten-1">
        <v-spacer></v-spacer>


      </v-app-bar>

      <v-main class="bg-amber-lighten-5">
        <v-container> 
            <slot name=""></slot>
        </v-container>
      </v-main>

      <v-footer color="amber-lighten-5" border app>2025 - Claim Point</v-footer>
    </v-app>
  </v-responsive>
</template>
