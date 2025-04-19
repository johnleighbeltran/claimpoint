<script setup>
import { ref } from 'vue'


</script>

<template>

<v-responsive>
<v-app>
    <v-app-bar class="px-3" color="amber-lighten-4">
        <!-- Logo -->
    <router-link to="/dashboard" class="d-flex align-center">
      <v-img
        src="/images/logofav.png"
        height="50"
        width="50"
        alt="Home"
        class="logo-btn"
        cover
      />
    </router-link>
      <v-spacer></v-spacer>
<!-- Dropdown Menu -->
    <v-menu>
      <template #activator="{ props }">
        <v-btn icon v-bind="props">
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </template>

      <v-list class="bg-amber-lighten-4" width="100">
        <v-list-item to="/profile" tag="router-link">
          <v-list-item-title>Profile</v-list-item-title>
        </v-list-item>

        <v-list-item to="/settings" tag="router-link">
          <v-list-item-title>Settings</v-list-item-title>
        </v-list-item>

        <v-list-item @click="logout">
          <v-list-item-title>Logout</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

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

<style scoped>
.logo-btn {
  cursor: pointer;
  transition: transform 0.2s ease;
}
.logo-btn:hover {
  transform: scale(1.1);
}
</style>