<script setup>
import TheHeader from './components/TheHeader.vue';
import DogTag from './components/DogTag.vue';
import TheFooter from './components/TheFooter.vue';
</script>

<template>
  <TheHeader></TheHeader>
  <v-container>
    <v-row>
      <v-col>
        <DogTag />
      </v-col>
      <v-col>
        <DogTag />
      </v-col>
      <v-col>
        <DogTag />
      </v-col>
    </v-row>
  </v-container>
  <TheFooter></TheFooter>
</template>

<style scoped></style>
