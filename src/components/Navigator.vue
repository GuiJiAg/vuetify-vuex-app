<template>
    <span>
        <v-navigation-drawer class="hidden-md-and-up" app bottom v-model="drawer" color="amber lighten-2" dark disable-resize-watcher>
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-item :key="index">
                        <v-list-item-content>
                            {{ item.title }}
                        </v-list-item-content>
                    </v-list-item>
                    <v-divider :key="`divider-${index}`"></v-divider>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar color="amber darken-4" dark>
            <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <v-toolbar-title>{{ appTitle }}</v-toolbar-title>
            <v-btn text class="hidden-sm-and-down">Menu</v-btn>
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn text class="hidden-sm-and-down">Sign In</v-btn>
            <v-btn color="amber lighten-3" class="hidden-sm-and-down">Join</v-btn>
        </v-app-bar>
    </span> 
</template>

<script>
export default {
    name: 'Navigator',
    data() {
        return {
            appTitle: 'Vue App',
            drawer: false,
            items: [
                { title: 'Menu' },
                { title: 'Sign In' },
                { title: 'Join'}
            ]
        };
    }
}
</script>

<style lang="stylus" scoped>
    
</style>