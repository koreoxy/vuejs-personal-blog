<script setup>
import { useRoute } from "vue-router";
import blogs from "../data/data.json";

const route = useRoute();
const blogId = parseInt(route.params.id);
const blog = blogs.find((q) => q.id === blogId);
</script>

<template>
  <h1>{{ blog.title }}</h1>
  <p>{{ blog.description }}</p>
</template>
