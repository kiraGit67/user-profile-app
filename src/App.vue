<template>
  <BaseHeader>
    <template #title>
      <h1>User Profile App</h1>
    </template>
  </BaseHeader>
  <BaseLayout>
    <users-list />
  </BaseLayout>
</template>

<script>
import BaseHeader from "@/components/layout/BaseHeader.vue";
import BaseLayout from "@/components/layout/BaseLayout.vue";
import UsersList from "@/components/UsersList.vue";
export default {
  components: {
    BaseHeader,
    BaseLayout,
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
