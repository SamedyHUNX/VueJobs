<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <section>
    <div class="container m-auto py-6 px-6">
      <RouterLink
        to="/jobs"
        class="text-green-500 mr-3 hover:text-green-600 flex items-center"
      >
        <i class="pi pi-arrow-circle-left" />
        Back to Job Settings
      </RouterLink>
    </div>
  </section>
</template>
