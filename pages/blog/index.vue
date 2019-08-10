<template>
    <section>
        <BlogArticle v-for="post in posts" :key="post.id" :articleInfo="post">
        </BlogArticle>
    </section>
</template>

<script>
import BlogArticle from '~/components/BlogArticlePreview.vue'


export default {
    components: {
        BlogArticle
    },
    data() {
        return {
            posts: [
                { id: '1', title: 'title', content: 'content' },
                { id: '2', title: 'title', content: 'content' },
                { id: '3', title: 'title', content: 'content' },
                { id: '4', title: 'title', content: 'content' }
            ]
        }
    }

}
</script>