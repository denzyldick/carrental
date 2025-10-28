<template>
  <v-layout class="rounded rounded-md border">
    <v-app-bar title="Car rental"></v-app-bar>

    <v-navigation-drawer>
      <v-list nav>
        <v-list-item title="Navigation drawer" link></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main class="d-flex">
      <CarList />
    </v-main>
  </v-layout>
</template>

<script setup>
//
</script>
