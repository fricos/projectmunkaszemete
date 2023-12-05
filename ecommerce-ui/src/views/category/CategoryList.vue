<template>
    <div class="container">
        <div class="row">
            <div class="col-12 text-center">
                <h3 class="pt-3">Our Categories</h3>
                <router-link :to="{name: 'AddCategory'}">
                    <button class="btn btn-primary" >Add category</button>
                </router-link>
            </div>
        </div>
        <div class="row">
            <div v-for="category of categories" :key="category.id" class="col-xl-4 col-md-6 col-12 pt-3 d-flex">
                <CategoryBox :category="category"></CategoryBox>
            </div>
        </div>
    </div>
</template>
<script>
const axios = require("axios");
//const sweetalert = require("sweetalert");
import CategoryBox from '../../components/Categories/CategoryBox.vue'
    export default {
        name: "CategoryList",
        components: { CategoryBox },
        data() {
            return {
                baseURL: "http://limitless-lake-55070.herokuapp.com",
                categories: [],
            };               
        },
        methods: {async getCategoies(){
            await axios.get(`${this.baseURL}/category`).then(res => this.categories=res).catch(err => console.log(err));
        }},
        mounted() {
            this.getCategoies();
        }
        
    }
</script>

