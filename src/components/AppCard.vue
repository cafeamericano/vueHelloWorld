<template>
    <div class='container'>
        <div class='card rounded mb-3 p-3'>

            <strong>{{ $attrs.title }}</strong>

            <img v-bind:src="$attrs.imagePath" height="150px" width="250px"/>
            <p>{{ $attrs.applicationType }}</p>
            <p>{{ $attrs.publishDate }} </p>

            <p>{{ $attrs.isFeatured}}</p>
            <p>{{ $attrs.isCollaboration }}</p>

            <p>{{ $attrs.deployedLink }}</p>
            <p>{{ $attrs.githubLink }}</p>
            <p>{{ $attrs.description }}</p>
            <p>{{ $attrs.supportStatus }}</p>
            <p>{{ $attrs.applicationType }}</p>

            <small>{{ $attrs.keywords }}</small>
        </div>
    </div>
</template>

<script>

export default {
    name: 'AppCard',
    props: []
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
