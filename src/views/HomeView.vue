<template>
  <div>
    <Slider />
    <Connect />
  </div>
</template>

<script>
  import Slider from '@/components/pageInitial/Slider.vue';
  import Connect from '@/components/pageInitial/Connect.vue';

export default {
  name: 'HomeView',
  components: { Slider, Connect }
}
</script>

<style scoped>
  
</style>