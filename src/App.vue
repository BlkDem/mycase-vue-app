<template>
  <V3DApp></V3DApp>

  <LeftNav></LeftNav>
</template>

<script>
import V3DApp from './components/V3DApp.vue';
import LeftNav from './components/LeftNav.vue';

export default {
  name: 'App',
  components: {
    V3DApp, LeftNav
  },
}
</script>

