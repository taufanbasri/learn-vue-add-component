<template>
  <section>
    <h2>My Friends</h2>
    <ul>
        <friend-contact
            v-for="friend in friends"
            :key="friend.id"
            :id="friend.id"
            :name="friend.name"
            :phone-number="friend.phone"
            :email-address="friend.email"
            :is-favorite="friend.isFavorite"
            @toggle-favorite="toggleFavoriteStatus"
        ></friend-contact>
    </ul>
  </section>
</template>

<script>
export default {
    data() {
        return {
            friends: [
                {
                    id: 1,
                    name: 'Taufan Prasetyo',
                    phone: '123123123',
                    email: 'taufan@mail.com',
                    isFavorite: true
                },
                {
                    id: 2,
                    name: 'Evita Karlina',
                    phone: '321321321',
                    email: 'evita@mail.com',
                    isFavorite: false
                }
            ]
        }
    },
    methods: {
        toggleFavoriteStatus(friendId) {
            const identifiedFriend = this.friends.find(friend => friend.id === friendId);

            identifiedFriend.isFavorite = !identifiedFriend.isFavorite;
        }
    },
}
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');
</style>