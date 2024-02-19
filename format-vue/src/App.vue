<script>
    import SearchBar from './Components/Header/SearchBar.vue'
    import SectionOne from './Components/Main/SectionOne.vue'

    export default {
        components:{
            SearchBar,
            SectionOne
        },
        data(){
            return{}
        }
    }
</script>

<template>
    <header>
        <SearchBar/>
    </header>
    <main>
        <SectionOne/>
    </main>
</template>

<style lang="scss">
    @use './Styles/main.scss'
</style>
