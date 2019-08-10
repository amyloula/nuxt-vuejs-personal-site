<template>
    <div class="container">
        <article>
            <h3>{{articleInfo.title}}</h3>
            <p>
                {{articleInfo.content}}
            </p>
        </article>
    </div>
</template>

<script>
export default {
    props: ["articleInfo"],
}
</script>