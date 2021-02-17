<template>
    <Layout>
        <h1>{{ $page.event.title }}</h1>
        <!-- <img :src="`http://localhost:1337${$page.events.thumbnail}`" /> -->
        <p>{{ $page.event.description }} </p>
    </Layout>
</template>

<page-query>
    query {
        event(id: "5") {
            id
            title
            duration
            price
            date
        }
    }
</page-query>

<script>
export default {
    metaInfo() {
        return {
            title: this.$page.event.title
        }
    }
}
</script>