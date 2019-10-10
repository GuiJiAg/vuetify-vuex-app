<template>
    <span>
        <home-hero></home-hero>
        <home-details></home-details>
        <home-gallery-sections></home-gallery-sections>
    </span>
</template>

<script>
import HomeHero from '@/components/home/HomeHero';
import HomeDetails from '@/components/home/HomeDetails';
import HomeGallerySections from '@/components/home/HomeGallerySections';

export default {
    name: 'Home',
    components: {
        HomeHero,
        HomeDetails,
        HomeGallerySections
    }
};
</script>

<style scoped>
    
</style>