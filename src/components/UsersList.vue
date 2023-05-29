<template>
  <ul>
    <user-card
      v-for="user of users"
      :key="user.id"
      :user="user"
      @changeFriendsStatus="changedFriend"
    />
  </ul>
</template>

<script>
import UserCard from "@/components/UserCard.vue";
export default {
  components: {
    UserCard,
  },
  data() {
    return {
      users: [
        {
          id: 1,
          firstname: "Justus",
          lastname: "Pfaue",
          friends: false,
          profileImg: "https://picsum.photos/200",
        },
        {
          id: 2,
          firstname: "Ferdinand",
          lastname: "Niemann",
          friends: false,
          profileImg: "https://picsum.photos/300",
        },
        {
          id: 3,
          firstname: "Isabella",
          lastname: "Di Cagno Robledo",
          friends: false,
          profileImg: "https://picsum.photos/400",
        },
        {
          id: 4,
          firstname: "Nina",
          lastname: "Märte",
          friends: true,
          profileImg: "https://picsum.photos/500",
        },
      ],
    };
  },
  methods: {
    changedFriend(id) {
      const index = this.users.findIndex((user) => user.id === id);
      this.users[index].friends = !this.users[index].friends;
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
  padding-left: 0;
}

ul li {
  padding-block: 1rem;
  padding-inline: auto;
  background-color: lightgrey;
  text-align: center;
  max-width: 400px;
}

ul li + li {
  margin-top: 1.5rem;
}
</style>
