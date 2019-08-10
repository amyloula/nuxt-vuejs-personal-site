<template>
    <div>
        {{post.title}} {{post.content}}
    </div>
</template>

<script>
export default {
    data() {
        return {
            id: this.$route.params.id
        }
    },
    // computed: {
    //     post() {
    //         return this.posts.find(post => post.id === this.id)
    //     }
    // },
    validate({ params }) {
        return !isNaN(+params.id)
    },
    asyncData({ params, env, error }) {
        // const user = env.users.find(user => String(user.id) === params.id)
        // if (!user) {
            // return error({ message: 'User not found', statusCode: 404 })
        // }
        // return user
    },
    head() {
        return {
            title: this.name
        }
    }
}
</script>