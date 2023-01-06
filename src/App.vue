<template>
  <TestVue class="app-test-vue" />
  <VueBind class="app-vue-bind" />
  <VueIf class="app-vue-if" />
</template>

<script>
import TestVue from './components/TestVue.vue';
import VueBind from './components/VueBind.vue';
import VueIf from './components/VueIf.vue';

export default {
  name: 'App',
  components: {
    TestVue,
    VueBind,
    VueIf,
  }
}
</script>

<style scoped lang="less">
  .app-test-vue {
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }
</style>
