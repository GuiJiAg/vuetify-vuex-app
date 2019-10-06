<template>
    <v-container fluid fill-height class="home-hero">
        <v-layout justify-center alignt-center column pa-5>
            <div class="display-3 font-weight-black white--text mb-3">Teresa Vargas González</div>
            <div class="display-2 font-weight-black white--text text-xs-center mb-5">Photographer</div>
            <div class="display-1 font-weight-bold white--text text-xs-center">This is my professional portfolio</div>
            <v-btn fab class="mt-5 amber darken-4">
                <v-icon large color="white">expand_more</v-icon>
            </v-btn>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomeHero',
    computed: {
        'font-size': function () {
            return {
                'mobile-font-size': this.$vuetify.breakpoint.name === 'xs',
                'no-mobile-font-size': this.error && this.error.type === 'fatal'
                }
            }
        }
};
</script>

<style scoped>
    .home-hero {
        background: url('http://localhost:8080/img/home-bg.b2dee779.jpg');
        background-size: cover;
        width: 100%;
        height: 100%;
    }
    .font-size {
        font-size: 34px;
    }  
</style>