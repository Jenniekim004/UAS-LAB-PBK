<template>
  <q-layout>
    <q-header class="main-header">
      <SiteNav />
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import SiteNav from './components/NavigationBar.vue';

export default {
  name: 'MainLayout',
  components: {
    SiteNav
  }
};
</script>

<style scoped>
.main-header {
  background-color: #f6f6f6;
  color: #fff;
  padding: 10px;
}
</style>
