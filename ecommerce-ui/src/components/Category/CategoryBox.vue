<template>
    <div class="card w-100 h-100" style="margin: 10px">
        <div class="ember-resposive ember-resposive-16">
            <img class="card-img-top" :src="category.imageUrl" alt="card img">
        </div>
        <div class="card-body">
            <h5 class="card-title">{{ category.categoryName }}</h5>
            <p class="card-text">{{ category.description }}</p>
            <a href="#" class="btn btn-primary">Szerkesztés</a>
        </div>
    </div>
</template>
<script>
export default {
    name: "CategoryBox",
    props: ["category"],
    methods: {},
};
</script>

<style scoped>
.card-img-top {
    object-fit: cover;
}
</style>