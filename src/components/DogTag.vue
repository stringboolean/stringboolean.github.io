<script setup>
  const name = 'Baguette';
  const description = 'Large and in charge! This handsome fella is waiting for his furever home where he can run wild but take breaks on the couch when the need for a breather arises.';
  const info = {
    age: 3,
    breed: 'Irish Wolfhound'
  }
  const loading = false;
  function seeDetails() {
    console.log('see details');
  }
</script>

<template>
  <v-card
    variant="tonal"
    :disabled="loading"
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
  >
    <template v-slot:loader="{ isActive }">
      <v-progress-linear
        :active="isActive"
        color="deep-purple"
        height="4"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img
      height="250"
      src="https://images.pexels.com/photos/128817/pexels-photo-128817.jpeg?cs=srgb&dl=pexels-brunocervera-128817.jpg&fm=jpg"
      cover
    ></v-img>

    <v-card-item>
      <v-card-title>{{ name }}</v-card-title>

      <v-card-subtitle>
        <span class="me-1">{{ info.age }} year-old {{ info.breed }}</span>
      </v-card-subtitle>
    </v-card-item>

    <v-card-text class="text-justify">
      {{ description }}
    </v-card-text>

    <v-divider class="mx-4 mb-1"></v-divider>

    <v-card-title>About Me</v-card-title>

    <div class="px-4 mb-2">
      <v-chip-group>
        <v-chip>Potty Trained</v-chip>

        <v-chip>Kid Friendly</v-chip>
      </v-chip-group>
    </div>

    <v-card-actions>
      <v-btn
        color="deep-purple-lighten-2"
        text="Get To Know Me"
        block
        border
        @click="seeDetails"
      ></v-btn>
    </v-card-actions>
  </v-card>
</template>

<style>
</style>