<template>
    <div id="app">
        <Navbar/>
        <AppForm/>
        <CardContainer :allApplications="allApplications" :key="componentKey" />
    </div>
</template>

<script>

import CardContainer from './components/CardContainer.vue'
import AppForm from './components/AppForm.vue'
import Navbar from './components/Navbar.vue'

export default {
    name: 'App',
    mounted: function() {
        this.pullApplications();
        this.pullKeywords();
    },
    data() {
        return {
            componentKey: 0,
            allApplications: []
        }
    },
    methods: {
        pullApplications() {
            var self = this;
            fetch("https://central-api-flask-cm6ud432ka-uc.a.run.app/AppGalleryLite/api/applications").then(function (response) {
                return response.json();
            }).then(function (result) {
                self.allApplications = result;
                self.componentKey +=1;
            });
        },
        pullKeywords() {
            var self = this;
            fetch("https://central-api-flask-cm6ud432ka-uc.a.run.app/AppGalleryLite/api/keywords").then(function (response) {
                return response.json();
            }).then(function (result) {
                self.todos = result;
                self.componentKey +=1;
            });
        }
    },
    components: {
        AppForm,
        CardContainer,
        Navbar
    }
}

</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
}
</style>
