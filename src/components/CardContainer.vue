<template>
    <div>
        <div v-for='item in allApplications' :key='item.title'>
            <AppCard v-bind='item' />
        </div>
    </div>
</template>

<script>

import AppCard from './AppCard.vue'

export default {
    name: 'CardContainer',
    props: [
        'allApplications'
    ],
    components: {
        AppCard
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
