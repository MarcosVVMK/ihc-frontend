<script>
  import { defineComponent } from 'vue';
  import ApplicationLogo from '@/components/ApplicationLogo.vue';
  export default defineComponent({
    components: { ApplicationLogo },
  });
</script>
<template>
  <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100 dark:bg-gradient-to-r from-cyan-500 to-blue-500">

    <ApplicationLogo class="shadow-2xl sm:rounded-lg border-solid" />

    <div class="w-full sm:max-w-md mt-6 px-6 py-4 shadow-2xl overflow-hidden sm:rounded-lg ">
      <slot />
    </div>
  </div>
</template>
