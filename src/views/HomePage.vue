<template>
    <div class="homepage">
        <v-responsive :aspect-ratio="16/9">
        <!-- <v-container style="height: 100%"> -->
            <NavBar />
            <HelloWorld />
            <Footer />
        <!-- </v-container> -->
        </v-responsive>
  </div>  
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import Footer from '@/components/Footer.vue'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'HomePage',
    components: {
        NavBar,
        HelloWorld,
        Footer
    }
}
</script>

