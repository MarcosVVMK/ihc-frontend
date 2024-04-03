<script setup lang="ts">
  import GuestLayout from '@/layouts/GuestLayout.vue'
  import InputLabel from '@/components/InputLabel.vue'
  import TextInput from '@/components/TextInput.vue'
  import InputError from '@/components/InputError.vue'
  import PrimaryButton from '@/components/PrimaryButton.vue'

const form = {
  email: 'marcosvm000@gmail.com',
  password: 'password',
  errors: {
    email: 'User not exists!',
    password: 'Inválid Password'
  },
  processing: false
};

</script>

<template>

  <main>
    <GuestLayout>
      <form>
        <div>
          <InputLabel for="email" value="Email" />
          <TextInput
            id="email"
            type="email"
            class="mt-1 block w-full"
            v-model="form.email"
            required
            autofocus
            autocomplete="username"
          />
          <InputError class="mt-2" :message="form.errors.email" />
        </div>

        <div class="mt-4">
          <InputLabel for="password" value="Senha" />
          <TextInput
            id="password"
            type="password"
            class="mt-1 block w-full"
            v-model="form.password"
            required
            autocomplete="current-password"
          />
          <InputError class="mt-2" :message="form.errors.password" />
        </div>
        <div class="flex items-center justify-center mt-4">
          <PrimaryButton
            class="ms-4 hover:scale-110"
            :class="{ 'opacity-25': form.processing }"
            :disabled="form.processing"
          >
            Acessar
          </PrimaryButton>
        </div>
      </form>
    </GuestLayout>
  </main>
</template>
