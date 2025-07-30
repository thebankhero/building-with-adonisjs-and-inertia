<script setup lang="ts">
import AuthLayout from '~/layouts/AuthLayout.vue';

defineOptions({ layout: AuthLayout })
</script>


<template>
  <div class="flex flex-col space-y-2">
    <h1 class="text-2xl font-semibold tracking-tight">Register</h1>
    <p class="text-sm text-muted-foreground">
      <Link href="/login">Have an account? Login</Link>
    </p>
  </div>
</template>
