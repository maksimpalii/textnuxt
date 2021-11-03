<template>
    <section>
        <h1>{{pageTtile}}</h1>

        <ul>
            <li v-for="user of users" :key="user.id">
            <a href="#" @click.prevent="openUser(user)">{{user.name}}</a>
            </li>
        </ul>
    </section>
</template>
<script>
export default {
    async asyncData({$axios}){
        const users = await $axios.$get('https://jsonplaceholder.typicode.com/users')
        return {users}
    },
    data(){
        return {
            pageTtile:'Users Page'
        }
    },
    // async mounted(){
    //     this.users = await this.$axios.$get('https://jsonplaceholder.typicode.com/users')
    // },
    methods: {
        openUser(user){
            this.$router.push('/users/' + user.id)
        }
    }
}
</script>