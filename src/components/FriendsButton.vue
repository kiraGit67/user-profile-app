<template>
  <button @click="this.$emit('changeFriendsState')">
    <slot></slot>
    {{ friendsState ? "Als Freund:in entfernen" : "als Freund:in hinzufügen" }}
  </button>
</template>

<script>
export default {
  props: {
    friendsState: Boolean,
  },
};
</script>
