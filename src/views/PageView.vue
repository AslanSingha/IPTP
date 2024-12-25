<template>
  <div class="page">
    
    <Sidebar :page="pageName" />
    <h1>Welcome to {{ pageName }}</h1>
    <router-view />
  </div>
</template>

<script>
import Sidebar from '../components/Sidebar.vue';

export default {
  components: {
    Sidebar,
  },
  computed: {
    pageName() {
      return this.$route.params.page; // Get current page from the route
    },
  },
};
</script>

<style scoped>
.page {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-left: 2px solid rgb(0, 0, 0);
  border-right: 2px solid rgb(0, 0, 0);
  padding: 20px;
}

</style>