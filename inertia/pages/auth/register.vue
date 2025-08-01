<script setup lang="ts">
import { router } from '@inertiajs/vue3';
import { ref } from 'vue';
import Label from '~/components/ui/label/Label.vue';
import AuthLayout from '~/layouts/AuthLayout.vue';

defineOptions({ layout: AuthLayout })

const form = ref({
  fullName: '',
  email: '',
  password: '',
})
</script>


<template>
  <AppHead title="Register"
    description="Start plotting and planning your courses with ease by creating your PlotMyCourse account today" />

  <div class="flex flex-col space-y-2">
    <h1 class="text-2xl font-semibold tracking-tight">Register</h1>
    <p class="text-sm text-muted-foreground">
      <Link href="/login">Have an account? Login</Link>
    </p>
  </div>

  <form class="grid gap-3" @submit.prevent="router.post('/register', form)">
    <Label class="grid gap-1">
      <span>Full Name</span>
      <Input type="text" v-model="form.fullName" />
    </Label>
    <Label class="grid gap-1">
      <span>Email</span>
      <Input type="email" v-model="form.email" />
    </Label>
    <Label class="grid gap-1">
      <span>Password</span>
      <Input type="password" v-model="form.password" />
    </Label>

    <Button type="submit">
      Register
    </Button>
  </form>
</template>
