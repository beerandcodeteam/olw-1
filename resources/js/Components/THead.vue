<script setup>
import {computed} from "vue";

const props = defineProps(['type', 'label'])

const classes = computed(() => {

        if (props.type === "first") {
            return "py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-6"
        }

        if (props.type === "normal") {
            return "hidden px-3 py-3.5 text-left text-sm font-semibold text-gray-900 sm:table-cell"
        }

        if (props.type === "action") {
            return "relative py-3.5 pl-3 pr-4 sm:pr-6"
        }
    }
);
</script>

<template>
    <th
        scope="col"
        :class="classes"
    >{{ props.label }}</th>
</template>