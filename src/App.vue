<template>
  <section>
    <h2>My Friends</h2>
    <ul>
        <friend-contact
            name="Taufan Prasetyo"
            phone-number="123 1234"        
            email-address="taufan@mail.com"
            is-favorite="1"
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
    @import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');
</style>