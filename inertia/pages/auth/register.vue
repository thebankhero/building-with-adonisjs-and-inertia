<script setup lang="ts">
import { SharedProps } from '@adonisjs/inertia/types';
import { usePage } from '@inertiajs/vue3';

const props = defineProps<{ stuff: string, sharedFromRoute: boolean, sharedFromMiddleware: string } & SharedProps>()
const page = usePage<SharedProps>()
</script>


<template>
  <h1>Register {{ stuff }}, {{ sharedFromRoute }}, {{ sharedFromMiddleware }}, {{ page.props.sharedGlobally }}</h1>
</template>
