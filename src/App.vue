<template>
  <header>
    <h1>User Profile App</h1>
  </header>
  <main>
    <users-list />
  </main>
</template>

<script>
import UsersList from "@/components/UsersList.vue";
export default {
  components: {
    UsersList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin: 2rem 1.5rem;
}
</style>
