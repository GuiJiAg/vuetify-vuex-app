<template>
    <v-container grid-list-lg>
        <v-layout row>
            <v-flex xs12 class="text-center display-1 font-wight-black my-5">My Gallery</v-flex>
        </v-layout>
        <v-layout row wrap>
            <v-flex xs12 sm12 md4>
                <nature-section></nature-section>
            </v-flex>
            <v-flex xs12 sm12 md4>
                <models-section></models-section>
            </v-flex>
            <v-flex xs12 sm12 md4>
                <concerts-section></concerts-section>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
import NatureSection from '@/components/gallery/NatureSection';
import ModelsSection from '@/components/gallery/ModelsSection';
import ConcertsSection from '@/components/gallery/ConcertsSection';

export default {
    name: 'HomeGallerySections',
    components: {
        NatureSection,
        ModelsSection,
        ConcertsSection
    }
}
</script>

<style scoped>
    
</style>