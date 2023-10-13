<script setup>
import Layout from "@/Layouts/Layout.vue";
import Pagination from "@/Layouts/Pagination.vue";
import { Head } from "@inertiajs/vue3";

const props = defineProps({
    products: Object,
});
</script>

<template>
    <Head title="Products" />
    <Layout title="Products">
        <div class="flex justify-between bg-light-400">
            <h2 class="font-bold text-4xl text-dark ml-8 mt-4 mb-4">
                Products
            </h2>
        </div>

        <div class="overflow-x-auto">
              <a
                href="/products/create"
                class="float-right bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mt-3 mr-3"
                >Add product</a
            > 
            <table class="table-auto min-w-full">
                <thead>
                    <tr>
                       
                        <th class="px-4 py-2">Brand</th>
                        <th class="px-4 py-2">Name</th>
                         <th class="px-4 py-2">Description</th> 
                        <th class="px-4 py-2">Retail Price</th>
                        <th class="px-4 py-2">Quantity Stock</th>
                        <th class="px-4 py-2">Category</th> 
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="product in products.data" :key="product.id">
                        
                        <td class="border px-4 py-2">{{ product.brand }}</td>
                        <td class="border px-4 py-2">{{ product.name }}</td>
                         <td class="border px-4 py-2">
                            {{ product.description }}
                        </td> 
                        <td class="border pl-2 py-2">
                          {{ product.retail_price }}
                        </td>
                        <td class="border pl-2 py-2">
                            {{ product.category.name }}
                          </td>
                        <td class="border px-4 py-2">
                            {{ product.qty_stock }}
                        </td>
                        
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="flex justify-center items-center mt-4">
            <Pagination
                :links="products.links"
                :currentPage="products.current_page"
                :totalPages="products.total"
                pageRange="4"
            />
        </div>
    </Layout>
</template>
