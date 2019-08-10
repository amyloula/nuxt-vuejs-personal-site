<template>
    <div>
        <home/>
    </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Home from '~/components/Home.vue'

export default {
    asyncData({ env }) {
        return { users: env.users }
    },
    
    components: {
        Header,
        Home
    }
}
</script>