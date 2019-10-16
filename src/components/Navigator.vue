<template>
    <span>
        <v-navigation-drawer
          app
          v-model="drawer" 
          color="purple lighten-1" 
          dark 
          disable-resize-watcher>
            <v-icon medium color="white" class="margin-button" @click="drawer = !drawer">clear</v-icon>
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-item :key="index">
                        <router-link :to="item.path">
                            <v-list-item-content>
                                {{ item.title }}
                            </v-list-item-content>
                        </router-link>
                    </v-list-item>
                    <v-divider :key="`divider-${index}`"></v-divider>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar color="purple darken-4" dark>
            <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <router-link to="/">
                <v-toolbar-title>{{ appTitle }}</v-toolbar-title>
            </router-link>
            <v-btn text to="/gallery" class="hidden-sm-and-down margin-button">Gallery</v-btn>
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn text to="/sign-in" class="hidden-sm-and-down margin-button">Sign In</v-btn>
            <v-btn to="/join" color="purple lighten-3" class="hidden-sm-and-down margin-button black--text">Join</v-btn>
        </v-app-bar>
    </span> 
</template>

<script>
export default {
    name: 'Navigator',
    data() {
        return {
            appTitle: 'My Portfolio',
            drawer: false,
            items: [
                { title: 'Gallery', path: '/gallery' },
                { title: 'Sign In', path: '/sign-in' },
                { title: 'Join', path: '/join'}
            ]
        };
    }
}
</script>

<style scoped>
    .margin-button {
        margin: 10px;
    }

    .v-application a {
        color: white;
        text-decoration: none;
    }
</style>