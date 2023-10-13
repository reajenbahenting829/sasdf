<script setup>
import Layout from "@/Layouts/Layout.vue";
import { Head } from "@inertiajs/vue3";

const props = defineProps({});
</script>

<template>
    <Head title="Create Product" />
    <Layout title="Create Product">
        <div class="flex justify-between bg-light-400">
            <h4 class="font-bold text-4xl text-dark ml-8 mt-4 mb-4">
                Create Product
            </h4>
          
            <div class="max-w-6xl mx-auto p-4 bg-blue-800  ">
                <br>
                <br>
                <br>
                <br>
                <form class="bg-blue-800  ">
                    <div class="mb-4">
                        <label class="block text-light text-sm font-bold mb-2" for="product_name">
                            Product Name
                        </label>
                        <input
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            id="product_name"
                            type="text"
                            placeholder="Product Name"
                        />
                    </div>
                    <div class="mb-4">
                        <label class="block text-light text-sm font-bold mb-2" for="description">
                            Description
                        </label>
                        <textarea
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-light leading-tight focus:outline-none focus:shadow-outline"
                            id="description"
                            placeholder="Product Description"
                        ></textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-light text-sm font-bold mb-2" for="price">
                            Price
                        </label>
                        <input
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-light leading-tight focus:outline-none focus:shadow-outline"
                            id="price"
                            type="text"
                            placeholder="Product Price"
                        />
                    </div>
                    <div class="mb-6">
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="category">
                            Category
                        </label>
                        <select
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            id="category"
                        >
                            <option value="">Select Category</option>
                            <!-- Add category options here -->
                        </select>
                    </div>
                    <div class="flex items-center justify-between">
                       
                    </div>
                </form>
            </div>
            
            
        </div>
    </Layout>
</template>