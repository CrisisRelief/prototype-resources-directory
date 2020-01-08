<template>
    <div class="search-result-container">
        <a v-if="link.length > 0" href="link" ><h1>{{ title }}</h1></a>
        <h1 v-else>{{ title }}</h1>
        <div class="search-result-meta">
            <div class="search-result-categories">
                <span v-for="(category, index) in categories" :key="index" class="search-result-category">
                    {{ category }}<span v-if="index+1 < categories.length"> / </span>
                </span>
            </div>
            <div class="search-result-location">
                {{ location }}
            </div>
        </div>
        <div class="search-result-description">
            {{ description }}
        </div>
        <hr/>
    </div>
</template>

<script>
export default {
    props: {
        title: {},
        categories: {},
        location: {},
        description: {},
        contact: {},
        link: {
            default: ""
        },
    }
}
</script>

<style scoped>

.search-result-container {
    padding: 20px;
}

h1 {
    font-size: 20px;
    font-weight: 600; /* semibold */
    text-transform: uppercase;
}

a h1 {
    color: #02909E; /* Turquoise */
}

.search-result-meta {
    font-weight: 600; /* semibold */
}

</style>
