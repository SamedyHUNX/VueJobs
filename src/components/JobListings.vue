<script setup>
import axios from "axios";
import JobListing from "./JobListing.vue";
import { RouterLink } from "vue-router";
import { ref, onMounted } from "vue";

// reactive jobs
const jobs = ref([]);

// define props correctly
const props = defineProps({
  limit: {
    type: Number,
    default: null,
  },
  showButton: {
    type: Boolean,
    default: false,
  },
});

onMounted(async () => {
  try {
    const response = await axios.get("http://localhost:5000/jobs");
    jobs.value = response.data;
  } catch (error) {
    console.error("Error fetching jobs", error);
  }
});
</script>

<template>
  <section class="bg-blue-50 px-4 py-10">
    <div class="container-xl lg:container m-auto">
      <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">
        Browse jobs
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <JobListing
          v-for="job in props.limit ? jobs.slice(0, props.limit) : jobs"
          :key="job.id"
          :job="job"
        />
      </div>
    </div>
  </section>

  <section v-if="showButton" class="m-auto max-w-lg my-10 px-6">
    <RouterLink
      to="/jobs"
      class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
      >View All Jobs</RouterLink
    >
  </section>
</template>
