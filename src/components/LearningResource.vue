<template>
    <li>
        <div>
            <header>
                <h3>{{ resourceTitle }}</h3>
                <button>Delete</button>
            </header>
        </div>
        <p>{{ resourceDescription }}</p>
        <nav>
            <a :href="resourceLink">View Resource</a>
        </nav>
    </li>
</template>

<script>
export default {
    props: {
        resourceTitle: String,
        resourceDescription: String,
        resourceLink: String,
    }
}
</script>

<style scoped>
section {
    background-color: red;
}
</style>