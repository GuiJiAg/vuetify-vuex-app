<template>
    <v-container fluid fill-height class="home-hero" :class="xsBackgroundImage">
        <v-layout justify-center align-center column pa-5>
            <div class="display-3 font-weight-black white--text text-center mb-3" :class="xsD2FontSize">Teresa Vargas González</div>
            <div class="display-2 font-weight-black white--text text-center mb-6" :class="xsD1FontSize">Photographer</div>
            <div class="display-1 font-weight-bold white--text text-center" :class="xsD1FontSize">This is my professional portfolio</div>
            <v-btn fab class="mt-5 purple darken-4">
                <v-icon large color="white">expand_more</v-icon>
            </v-btn>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomeHero',
    computed: {
        xsD2FontSize: function () {
            return {
                'display-2': this.$vuetify.breakpoint.name === 'xs',
                'mb-12': this.$vuetify.breakpoint.name === 'xs',
                'mt-10': this.$vuetify.breakpoint.name === 'xs'
            }
        },
        xsD1FontSize: function () {
            return {
                'display-1': this.$vuetify.breakpoint.name === 'xs'            
            }
        },
        xsBackgroundImage: function () {
            return {
                'home-hero-xs': this.$vuetify.breakpoint.name === 'xs'            
            }
        }
    }
};
</script>

<style scoped>
    .home-hero {
        max-height: 100vh;
        background: url('../../assets/home-bg.jpg');
        background-size: cover;
    }

    .home-hero-xs {
        max-height: 100vh;
        background: url('../../assets/home-bg-xs.jpg');
        background-size: cover;
    }  
</style>