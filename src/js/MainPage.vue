<template>
    <!-- <div class="container"> <Nav /></div>
    <div class="container"> <Head /></div>
    <div class="container"> <Trainings :data="courses"/></div>
    <div class="container"> <Features /></div> -->
    
            <div>
                <Nav />
                <Head />
                <Trainings :data="courses"/>
                <Features />
                <Videos />
                <Footer />
            </div>
       
</template>

<script>
import Nav from './components/main/Nav.vue'
import Head from './components/main/Head.vue'
import Trainings from './components/main/Trainings.vue'
import Features from './components/main/Features.vue'
import Videos from './components/main/Videos.vue'
import Footer from './components/tarrifs/Footer.vue'

export default {
    components: { Nav, Head, Trainings, Features, Videos, Footer },
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