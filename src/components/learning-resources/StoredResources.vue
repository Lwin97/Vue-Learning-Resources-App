<template>
    <ul>
        <learning-resource v-for="resource in storedResources" :key="resource.id" :resource-title="resource.title"
            :resource-description="resource.description" :resource-link="resource.link">
        </learning-resource>
    </ul>
</template>

<script>
import LearningResource from "./LearningResource.vue";

export default {
    props: ["storedResources"],
    components: {
        LearningResource,
    },
}
</script>

<style scoped>
ul {
    list-style: none;
    margin: 0;
    padding: 0;
    margin: auto;
    max-width: 40rem;
}
</style>