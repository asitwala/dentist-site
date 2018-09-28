<template>
  <div class="ds-home">
    <home-screen-1/>
  </div>
</template>

<script>

import HomeScreen1 from '@/views/Home/HomeScreen1.vue';

export default {
  name: 'home',
  components: {
    'home-screen-1': HomeScreen1,
  },
};
</script>

<style scoped lang="scss">

</style>
