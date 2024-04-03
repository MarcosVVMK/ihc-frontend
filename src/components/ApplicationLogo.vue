<template>
  <a :href="home_url">
    <img alt="SIGH logo" class="logo" :src="image_url" width="125" height="125" />
  </a>
</template>
<script setup lang="ts">
  import image_url from '@/assets/images/logo.png';

  const home_url = window.location.origin

</script>