<template>
  <li>
    <img :src="user.profileImg" :alt="user.firstname + ' ' + user.lastname" />
    <div class="user-info">
      <p>{{ user.firstname }} {{ user.lastname }}</p>
      <friends-button
        :friendsState="user.friends"
        @changeFriendsState="$emit('changeFriendsStatus', user.id)"
      />
    </div>
  </li>
</template>

<script>
import FriendsButton from "@/components/FriendsButton.vue";
export default {
  props: {
    user: Object,
  },
  components: {
    FriendsButton,
  },
};

FriendsButton;
</script>

<style scoped>
ul li > img {
  width: 150px;
  aspect-ratio: 1;
  border-radius: 100%;
}

ul li > .user-info {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
}

.user-info button {
  _max-height: 30px;
}
</style>
