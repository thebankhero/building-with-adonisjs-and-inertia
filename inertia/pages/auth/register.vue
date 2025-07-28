<script setup lang="ts">
import { SharedProps } from '@adonisjs/inertia/types';
import { Link, usePage } from '@inertiajs/vue3';

const props = defineProps<{ stuff: string, sharedFromRoute: boolean, sharedFromMiddleware: string } & SharedProps>()
const page = usePage<SharedProps>()
</script>


<template>
  <h1>Register {{ stuff }}, {{ sharedFromRoute }}, {{ sharedFromMiddleware }}, {{ page.props.sharedGlobally }}</h1>

  <div class="flex flex-col space-y-2">
    <h1 class="text-2xl font-semibold tracking-tight">Register</h1>
    <p class="text-sm text-muted-foreground">
      <Link href="/login">Have an account? Login</Link>
    </p>
  </div>
</template>
