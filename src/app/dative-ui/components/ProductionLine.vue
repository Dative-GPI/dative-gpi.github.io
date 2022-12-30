<template>
    <div ref="root" class="h-full w-full production-line"></div>
</template>

<script setup lang="ts">
import lottie from "lottie-web";
import animation from "@/assets/animations/production_line.json"

const root = ref<HTMLElement | null>(null);

onMounted(() => {
    const anim = lottie.loadAnimation({
      container: root.value as HTMLElement, // the dom element that will contain the animation
      renderer: 'svg',
      loop: true,
      autoplay: true,
      rendererSettings: {
      },
      assetsPath: new URL( "~/assets/img/animations/production_line", import.meta.url ).href + "/",
      animationData: animation, // the path to the animation json
    });

    anim.setSpeed(0.5)
})
</script>

<style>
.production-line path {
  fill: transparent;
}
</style>