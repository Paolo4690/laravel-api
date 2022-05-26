<template>
    <div class="card">
        <img class="card-img-top" :src="post.image" :alt="post.title">
        <div class="card-body d-flex flex-column">
            <h4 class="card-title">{{ post.title }}</h4>
            <p class="card-text">{{ post.content }}</p>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item">Pubblicato da: {{ post.user_id }}</li>
            <li class="list-group-item">Categoria: {{ post.category_id }}</li>
            <li class="list-group-item">Post creato il: {{ $luxon(post.created_at, "dd-MM-yyyy") }}</li>

            <li v-show="post.created_at != post.updated_at" class="list-group-item">Post modificato il: {{ $luxon(post.updated_at, "dd-MM-yyyy") }}</li>

        </ul>
        <div class="card-body d-flex">
            <a :href="'/posts/' + post.slug" class=" btn btn-primary w-100 mt-auto">Visualizza post</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardPost',
    props: {
        'post': Object,

        },
}
</script>

<style>

</style>
