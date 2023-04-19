<template>
    <h1>{{ user }}</h1>
</template>

<script>
export default {
    name: 'UserRepositories',
    props: {
        user: {
            type: String,
            required: true
        },
    },
    setup(){
        
    },
    data(){
        return{
            repositories: [], // 1
            filters: {}, // 3
            searchQuery: '', // 2
        }
    },
    computed: {
        filteredRepositories(){
            // 3
            return null
        },
        repositoriesMatchingSearchQuery(){
            // 2
            return null
        },
    },
}

</script>