<script setup>
import Layout from "@/Layouts/Layout.vue";
import Pagination from "@/Layouts/Pagination.vue";
import { Head } from "@inertiajs/vue3";

const props = defineProps({
    users: Object,
});
</script>

<template>
    <Head title="Users" />
    <Layout title="Users">
        <div class="flex justify-between ">
            <h2 class="font-bold text-4xl text-light ml-8 mt-4 mb-4">
                Users List
            </h2>
        </div>

        <div class="overflow-x-auto">
            <a href="/admin/users/create" class="float-right  text-white font-bold py-2 px-4 rounded mt-3 mr-3">Add user</a>
            <table class="table-auto min-w-full">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Email</th>
                        <th>Roles</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="user in users.data" :key="user.id">
                        <td >{{ user.name }}</td>
                        <td >{{ user.email }}</td>
                        <td >
                            <span
                                v-for="role in user.roles"
                                :key="role.id"
                                :class="{
                                    'text-blue ':
                                        role.name === 'Admin',
                                    'text-green ':
                                        role.name === 'Super Visor',
                                    'text-yellow ':
                                        role.name === 'Cashier',
                                }"
                                class="ml-1 inline-block px-2 py-1 text-xs "
                            >
                                {{ role.name }}
                            </span>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="flex justify-center items-center mt-4">
            <Pagination
                :links="users.links"
                :currentPage="users.current_page"
                :totalPages="users.total"
                pageRange="4"
            />
        </div>
    </Layout>
</template>
