<template>
    <div class="homepage">
        <v-responsive :aspect-ratio="16/9">
            <Isi />
        </v-responsive>
  </div>  
</template>

<script>
import Isi from '@/components/Isi.vue'

export default {
    name: 'HomePage',
    components: {
        Isi,
    }
}
</script>

