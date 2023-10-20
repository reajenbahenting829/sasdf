<template>
    <div class="bg-pink-700 shadow-md p-2 rounded-lg mx-2">
        <div class="flex justify-center mb-2">
            <img
                src="images/m.jpg"
                alt="logo"
                class="logo-image"
            />
        </div>

        <h3 class="text-sm font-semibold">
            {{ client.last_name }}, {{ client.first_name }}
        </h3>
        <p class="text-dark-700 text-xs">{{ client.address }}</p>
        <p class="text-dark-700 text-xs">Phone: {{ client.phone }}</p>
        <p class="text-dark-700 text-xs">
            Credit Limit: <i class="fas fa-peso-sign"></i>{{ client.credit_limit }}
        </p>
        <a
            :href="'/clients/view/' + client.id"
            class="border-2 border-solid flex justify-center rounded-md border-gray-900 p-2"
            :class="{
                'bg-red-600': selectedColor == 'red',
                'bg-blue-600': selectedColor == 'blue',
                'bg-green-600': selectedColor == 'green',
            }"
        >
            View Detail
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
