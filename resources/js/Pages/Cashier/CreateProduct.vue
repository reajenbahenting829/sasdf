
<script setup>
import Layout from "@/Layouts/Layout.vue";
import { Head } from "@inertiajs/vue3";

const props = defineProps({});
</script>

<template>
    <Head title="Create Product" />
    <Layout title="Create Product">
        <div class="flex justify-between bg-pink-700">
            <h4 class="font-bold text-4xl text-white ml-8 mt-4 mb-4">
                Create Product
            </h4>
            
            <div class="max-w-3xl mx-auto p-8">
                <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
                    <div class="mb-4">
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="product_name">
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
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="description">
                            Description
                        </label>
                        <textarea
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                            id="description"
                            placeholder="Product Description"
                        ></textarea>
                    </div>
                    <div class="mb-4">
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="price">
                            Price
                        </label>
                        <input
                            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
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
                        <button
                            class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                            type="button"
                        >
                            Add Product
                        </button>
                    </div>
                </form>
            </div>
            
            
        </div>
    </Layout>
</template>

