<template>
  <section>
    <h2>My Friends</h2>
    <ul>
        <li v-for="friend in friends" :key="friend.id">{{ friend.name }}</li>
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
                    email: 'taufan@mail.com'
                },
                {
                    id: 2,
                    name: 'Evita Karlina',
                    phone: '321321321',
                    email: 'evita@mail.com'
                }
            ]
        }
    },
}
</script>

<style>

</style>