<script>
    import SearchBar from './Components/Header/SearchBar.vue'
    import SectionOne from './Components/Main/SectionOne.vue'
    import SectionTwo from './Components/Main/SectionTwo.vue'
    import SectionThree from './Components/Main/SectionThree.vue'

    export default {
        components:{
            SearchBar,
            SectionOne,
            SectionTwo,
            SectionThree
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
        <SectionThree/>
    </main>
</template>

<style lang="scss">
    @use './Styles/main.scss'
</style>
