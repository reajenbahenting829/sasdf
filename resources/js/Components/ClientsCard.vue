<template>
    <div class="shadow-md p-2 rounded-lg mx-2">
        <div class="flex justify-center mb-2">
            <img
                src="images/k.png"
                alt="logo"
                class="logo-image"
            />
        </div>


        <div class="min-w-[350px] mb-4 mx-2 p-4 bg-white rounded shadow border flex-1 cursor-pointer">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white flex items-center">
                {{ client.first_name }} {{ client.last_name }}
                <span class="text-xs px-3 py-1 5 bg-green-300 ml-3 rounded-lg">Level {{ client.level }}</span>
            </h5>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                <i class="fa-solid fa-location-dot"></i> &nbsp;
                {{ client.address }}</p>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                <i class="fa-solid fa-phone"></i> &nbsp;
                {{ client.phone }}</p>
        </div>
        <a
            :href="'/clients/view/' + client.id"
            class="border-2 border-solid flex justify-center rounded-md border-gray-900 p-2"
            :class="{
                'bg-red-600': selectedColor == 'red',
                'bg-blue-600': selectedColor == 'blue',
                'bg-green-600': selectedColor == 'green',
            }"
        >Click me
        </a>
    </div>
</template>

<script setup>
import { defineProps } from "vue";
import { inject } from "vue";

const selectedColor = inject("selectedColor");
// const selectedColor = ref('')

const props = defineProps({
    client: Object,
});
</script>
