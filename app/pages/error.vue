<script lang="ts" setup>
import { Icon, NuxtLink } from "#components";

const route = useRoute();
const error = route.query.error || "An unknown error occured!";
</script>

<template>
  <div class="card bg-base-300 container mt-4 min-h-72 text-center mx-auto flex flex-col items-center justify-center gap-4">
    <div role="alert" class="alert alert-error">
      <span>Oh No! {{ error }}</span>
    </div>
    <NuxtLink to="/" class="btn btn-primary">
      Home
      <Icon name="tabler:home" size="24" />
    </NuxtLink>
  </div>
</template>
