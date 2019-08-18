
<template>
    <header class="header">
        <div class="header__inner-wrapper">
            <div>
                <n-link to="/" no-prefetch>/
                </n-link>
            </div>
            <div>
                <n-link to="/about-me" no-prefetch>About me
                </n-link>
            </div>
            <div>
                <n-link to="/blog" no-prefetch>Blog</n-link>
            </div>
            <div>
                <n-link to="/projects" no-prefetch>Projects</n-link>
            </div>
            <div>
                <n-link to="/events" no-prefetch>Events</n-link>
            </div>
            <div>
                <n-link to="/contact" no-prefetch>Contact me</n-link>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@import "~assets/styles/_variables.scss";
.header {
    width: 100%;
    height: auto;
    .header__inner-wrapper {
        display: flex;
        width: 50%;
        margin-left: auto;
        flex-wrap: wrap;
        font-family: $main-header-font;
        >div {
            flex: 1;
            justify-content: center;
            text-align: right;
            padding: $main-padding;
            a {
                color: $secondary-text-color;
            }
            &:hover {
                color: $main-accent-color;
                transition: color 0.5s ease;
            }
        }
    }
}
</style>