<template>
   
            <div>
                <Nav />
                <HeadTarrifs />
                <OffersTarrifs />
                <InfoTarrifs />
                <TarrifsTarrifs/>
                <Footer />
            </div>
       
</template>

<script>
import Nav from './components/main/Nav.vue'
import HeadTarrifs from './components/tarrifs/HeadTarrifs.vue'
import OffersTarrifs from './components/tarrifs/OffersTarrifs.vue'
import InfoTarrifs from './components/tarrifs/InfoTarrifs.vue'
import TarrifsTarrifs from './components/tarrifs/TarrifsTarrifs.vue'
import Footer from './components/tarrifs/Footer.vue'

export default {
    components: { Nav, HeadTarrifs, OffersTarrifs, InfoTarrifs, TarrifsTarrifs, Footer },
    data() {
        return {
            courses: [
                {'title': 'Кардио', 'cl': '250 калорий', 'time': '58:24', 'img': 'cardio.png'},
                {'title': 'Растяжка', 'cl': '250 калорий', 'time': '58:24', 'img': 'stretch.png'},
                {'title': 'Йога', 'cl': '250 калорий', 'time': '58:24', 'img': 'joga.png'},
                {'title': 'Бег', 'cl': '250 калорий', 'time': '58:24', 'img': 'run.png'},
                {'title': 'Гантели', 'cl': '250 калорий', 'time': '58:24', 'img': 'metal.png'},
                {'title': 'На улице', 'cl': '250 калорий', 'time': '58:24', 'img': 'street.png'},
             ]
    }
   }
}

</script>

<style lang="scss">
  
</style>