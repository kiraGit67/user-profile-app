<template>
  <BaseHeader>
    <template #title>
      <h1>User Profile App</h1>
    </template>
  </BaseHeader>
  <BaseLayout>
    <users-list />
  </BaseLayout>
  <BaseFooter>
    <template v-slot:subtitle-left><h3>Users</h3></template>
    <template v-slot:subtitle-middle><h3>Friends</h3></template>
    <template v-slot:subtitle-right><h3>Non-Friends</h3></template>
  </BaseFooter>
</template>

<script>
import BaseHeader from "@/components/layout/BaseHeader.vue";
import BaseLayout from "@/components/layout/BaseLayout.vue";
import UsersList from "@/components/UsersList.vue";
import BaseFooter from "@/components/layout/BaseFooter.vue";
export default {
  components: {
    BaseHeader,
    BaseLayout,
    UsersList,
    BaseFooter,
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
