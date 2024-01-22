<template>
    <ul>
        <learning-resource v-for="resource in storedResources" :key="resource.id" :resource-title="resource.title"
            :resource-description="resource.description" :resource-link="resource.link">
        </learning-resource>
    </ul>
</template>

<script>
import LearningResource from "./components/LearningResource.vue";

export default {
    components: {
        LearningResource,
    },
    data() {
        return {
            storedResources: [
                {
                    id: "1234",
                    title: "Official Guide",
                    description: "The official Vue.js documentation.",
                    link: "https://vuejs.org",
                },
                {
                    id: "google",
                    title: "Google",
                    description: "Learn to google...",
                    link: "https://google.org",
                },
            ],
        };
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
    box-sizing: border-box;
}

html {
    font-family: 'Roboto', sans-serif;
}

body {
    margin: 0;
}
</style>