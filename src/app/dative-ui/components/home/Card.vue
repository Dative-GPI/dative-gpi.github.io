<template>
    <NuxtLink>
        <Card class="h-80 w-80 border-linear-gradient cursor-pointer hover:shadow-2xl" :style="{
            '--left': left,
            '--right': right
        }" @mouseover="start = true" @mouseleave="start = false">
            <div class="h-4/5">
                <slot name="image" v-bind="{ start }"/>
            </div>
            <div
                class="px-4 text-blue-600 h-1/5 flex text-center justify-center flex-col font-sans font-medium text-md uppercase ">
                <slot name="footer" />
            </div>
        </Card>
    </NuxtLink>
</template>

<script setup lang="ts">

const props = defineProps<{ left: string, right: string }>()
const start = ref(false);

</script>