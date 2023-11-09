<script setup>
import Layout from "@/Layouts/Layout.vue";
import { Head } from "@inertiajs/vue3";
import Card from '@/Components/Card.vue';
import { inject } from 'vue';

const themeMode = inject('themeMode');
 const products = [{

    "id": 2,
            "title": "iPhone X",
            "description": "SIM-Free, Model A19211 6.5-inch Super Retina HD display with OLED technology A12 Bionic chip with ...",
            "price": 899,
            "discountPercentage": 17.94,
            "rating": 4.44,
            "stock": 34,
            "brand": "Apple",
            "category": "smartphones",
            "thumbnail": "https://i.dummyjson.com/data/products/2/thumbnail.jpg"

 },
 {
    "id": 5,
            "title": "Huawei P30",
            "description": "Huawei’s re-badged P30 Pro New Edition was officially unveiled yesterday in Germany and now the device has made its way to the UK.",
            "price": 499,
            "discountPercentage": 10.58,
            "rating": 4.09,
            "stock": 32,
            "brand": "Huawei",
            "category": "smartphones",
            "thumbnail": "https://i.dummyjson.com/data/products/5/thumbnail.jpg",  
 },
 {

    "id": 3,
            "title": "Samsung Universe 9",
            "description": "Samsung's new variant which goes beyond Galaxy to the Universe",
            "price": 1249,
            "discountPercentage": 15.46,
            "rating": 4.09,
            "stock": 36,
            "brand": "Samsung",
            "category": "smartphones",
            "thumbnail": "https://i.dummyjson.com/data/products/3/thumbnail.jpg"

},
{
    "id": 6,
            "title": "MacBook Pro",
            "description": "MacBook Pro 2021 with mini-LED display may launch between September, November",
            "price": 1749,
            "discountPercentage": 11.02,
            "rating": 4.57,
            "stock": 83,
            "brand": "Apple",
            "category": "laptops",
            "thumbnail": "https://i.dummyjson.com/data/products/6/thumbnail.png",  
},
{
    "id": 7,
            "title": "Samsung Galaxy Book",
            "description": "Samsung Galaxy Book S (2020) Laptop With Intel Lakefield Chip, 8GB of RAM Launched",
            "price": 1499,
            "discountPercentage": 4.15,
            "rating": 4.25,
            "stock": 50,
            "brand": "Samsung",
            "category": "laptops",
            "thumbnail": "https://i.dummyjson.com/data/products/7/thumbnail.jpg",
},
{

    "id": 4,
            "title": "OPPOF19",
            "description": "OPPO F19 is officially announced on April 2021.",
            "price": 280,
            "discountPercentage": 17.91,
            "rating": 4.3,
            "stock": 123,
            "brand": "OPPO",
            "category": "smartphones",
            "thumbnail": "https://i.dummyjson.com/data/products/4/thumbnail.jpg"
}
]


</script>

<template>
    <Head title="Dashboard" />

    <Layout>
        <template #header>
            <h2
                class="font-semibold text-2xl text-gray-800 leading-tight"
            ></h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class=" overflow-hidden shadow-sm sm:rounded-lg">
                    <div class="grid">
                             <Card v-for="prod in products"> 
                                <template #head> 
                                    <h3 class=" text-center text-2xl text-black">{{ prod.title }}</h3>
                                </template>
                                <template #content1> 
                                    <img :src="prod.thumbnail" alt="" class="card-image">
                                </template>
                                <template #content2> 
                                   <div class="p-4 rounded bg-blue-500 text-gray-100">
                                    {{ prod.description }}
                                   </div>
                                </template>
                                <template #footer> 
                                    <div class="flex justify-between">
                                        <h2 class="text-2xl text-blue-500 font-bold">
                                            PhP {{ prod.price }}
                                        </h2>
                                    </div>
                                    
                                </template>
                                
                            </Card>
                    </div>
                </div>
            </div>
        </div> 

        
    </Layout>
</template>

<style scoped>
.grid{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px 24px;
}

.card-image{
    width: 100%;
    aspect-ratio: 16/9;
    object-fit: cover;
}
</style>

