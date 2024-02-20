<script>
    import SearchBar from './Components/Header/SearchBar.vue'
    import SectionOne from './Components/Main/SectionOne.vue'
    import SectionTwo from './Components/Main/SectionTwo.vue'

    export default {
        components:{
            SearchBar,
            SectionOne,
            SectionTwo
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
        <SectionTwo/>
    </main>
</template>

<style lang="scss">
    @use './Styles/main.scss'
</style>
