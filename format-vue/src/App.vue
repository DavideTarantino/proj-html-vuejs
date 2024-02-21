<script>
    import SearchBar from './Components/Header/SearchBar.vue'
    import SectionOne from './Components/Main/SectionOne.vue'
    import SectionTwo from './Components/Main/SectionTwo.vue'
    import SectionThree from './Components/Main/SectionThree.vue'
    import SectionFour from './Components/Main/SectionFour.vue'
    import SectionFive from './Components/Main/SectionFive.vue'
    import SectionSix from './Components/Main/SectionSix.vue'
    import SectionSeven from './Components/Main/SectionSeven.vue'

    export default {
        components:{
            SearchBar,
            SectionOne,
            SectionTwo,
            SectionThree,
            SectionFour,
            SectionFive,
            SectionSix,
            SectionSeven
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
        <SectionFour/>
        <SectionFive/>
        <SectionSix/>
        <SectionSeven/>
    </main>
</template>

<style lang="scss">
    @use './Styles/main.scss'
</style>
