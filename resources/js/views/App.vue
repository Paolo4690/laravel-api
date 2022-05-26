<template>
    <div class="container">
        <header-component></header-component>
        <container-post></container-post>
    </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue';
import ContainerPost from '../components/ContainerPost.vue';

export default {
    name: 'App',
    components: {
        HeaderComponent,
        ContainerPost
    },

}
</script>

<style>

</style>
