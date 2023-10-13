<script setup>
import { Link } from '@inertiajs/vue3';

const props = defineProps({
  links: Array,
});
</script>

<template>
  <div>
    <div class="flex flex-wrap -mb-1">
      <template v-for="(link, p) in links" :key="p">
        <div
          v-if="link.url === null"
          class="mr-1 mb-1 px-4 py-3 text-sm  "
          v-html="link.label"
        ></div>
        <Link
          v-else
          class="mr-1 mb-1 px-4 py-3 text-sm   "
          :class="{ 'bg-blue-700 text-white': link.active }"
          :href="link.url"
          v-html="link.label"
        ></Link>
      </template>
    </div>
  </div>
</template>
