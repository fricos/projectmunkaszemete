<template>
    <div class="body">
        <div class="wrapper">
        <form action="" method="post">
            <h1>Add Category</h1>
            <div class="input-box">
                <label for="">Név</label>
                <input type="text" v-model="categoryName" placeholder="név">
            </div>
            <div class="input-box">
                <label for="">Leírás</label>
                <input type="text" v-model="description" placeholder="leírás">
            </div>
            <div class="input-box">
                <label for="">Kép url</label>
                <input type="text" v-model="imageUrl" placeholder="a kép linkje">
            </div>
            <button type="button" class="btn" @click="addCategory">Kész</button>
        </form>
    </div>
    
    </div>
</template>
<script>
    const axios = require("axios");
    const sweetalert = require("sweetalert");
    export default {
        data() {
            return {
                categoryName: "",
                description: "",
                imageUrl: ""
            };
        },
        methods: {
            addCategory() {
                console.log(this.categoryName, this.description, this.imageUrl);
                const newCategory = {
                    categoryName: this.categoryName,
                    description: this.description,
                    imageUrl: this.imageUrl
                }
                const baseURL = "http://limitless-lake-55070.herokuapp.com";
    
                axios({
                    method: "post",
                    url: `${baseURL}/category/create`,
                    data: JSON.stringify(newCategory),
                    headers: {
                        'Content-Type': 'application/json',
                    }
                }).then(() => {
                    sweetalert({
                        text: "category created successfully",
                        icon: "success",
                    })
                }).catch(err =>{
                    console.log(err);
            });
            }
        },
    }
</script>
<style>
    @import url("https://fonts.googleapis.com/css?family=Poppins:wgth@300;400;500;600;700;800;900&display=swap");

.body {
    display: flex;
    justify-content: center;
    align-items: center;
    background: url("https://cdn.discordapp.com/attachments/1153584270158331975/1169000442756341850/65_seo_image_21_03_18_07_12_29.jpg?ex=6578b980&is=65664480&hm=e43ddf36118915a7f6a7d6add818f9f88f8a9f69e763cdcb6a1a1cdd517c2ec1&");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.wrapper {

    width: 420px;
    background-color: transparent;
    border: 2px solid rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
    box-shadow: 0 0 10px rgba(0 0 0 0.1);
    color: rgba(0, 0, 0, 1);
    padding: 30px 40px;
    border-radius: 10px;
}

.wrapper h1 {
    text-align: center;
    font-size: 36px;
}

.wrapper .input-box {
    position: relative;
    width: 100%;
    height: 50px;
    margin: 40px 0;
}

.input-box input {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    border: 2px solid rgba(255, 255, 255, 0.2);
    border-radius: 40px;
    font-size: 16px;
    color: rgba(0, 0, 0, 1);
    padding: 20px 45px 20px 20px;
}

.input-box input::placeholder {
    color: rgba(0, 0, 0, 0.3);
}

.input-box i {
    position: absolute;
    right: 20px;
    top: 100%;
    transform: translateY(-50%);
    font-size: 20px;
}

.wrapper .btn {
    top: 20px;
    position: relative;
    width: 100%;
    height: 50px;
    border: none;
    outline: none;
    background: #fff;
    border-radius: 40px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    font-size: 16px;
    font-weight: 600;
    color:black;
}
</style>