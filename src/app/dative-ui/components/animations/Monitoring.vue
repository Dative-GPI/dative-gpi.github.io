<template>
    <div ref="root"
        class="h-full w-full"></div>
</template>

<script setup lang="ts">
import lottie from "lottie-web";
import animation from "@/assets/animations/monitoring.json"

const props = withDefaults(defineProps<{ start?: boolean }>(), {
    start: false
});

const root = ref<HTMLElement | null>(null);

onMounted(() => {
    const anim = lottie.loadAnimation({
        container: root.value as HTMLElement, // the dom element that will contain the animation
        renderer: 'svg',
        loop: true,
        autoplay: props.start,
        rendererSettings: {
        },
        assetsPath: new URL("~/assets/img/animations/monitoring", import.meta.url).href + "/",
        animationData: animation, // the path to the animation json
    });

    anim.setSpeed(0.5)

    watch(() => props.start, () => {
        if(props.start)
            anim.play();
        else
            anim.pause();
    })
})

</script>

<style>
</style>