<template>
    <v-app>
        <navigator></navigator>
        <v-content transition="slide-x-transition">
            <router-view></router-view>
        </v-content>
    </v-app>
</template>

<script>
import Navigator from '@/components/Navigator';

export default {
    name: 'App',
    components: {
        Navigator
    }
};
</script>

<style scoped>

</style>
