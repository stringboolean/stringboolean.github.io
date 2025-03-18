<script setup>
  const links = ['About Us', 'Donate', 'Volunteer', 'Contact Us'];
</script>

<template>
  <v-footer class="d-flex align-center justify-center ga-2 flex-wrap flex-grow-1 py-3" color="surface-light">
    <v-btn
      v-for="link in links"
      :key="link"
      :text="link"
      variant="text"
      rounded
    ></v-btn>

    <div class="flex-1-0-100 text-center mt-2">
      {{ new Date().getFullYear() }} — <strong>String Boolean</strong>
    </div>
  </v-footer>
</template>