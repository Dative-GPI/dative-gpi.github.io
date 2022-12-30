<template>
  <div>
    <Section :bottom-left="40"
      class="gradient-home-01 relative h-[35rem]">
      <div class="text-pink-600 font-sans font-bold text-3xl absolute top-1/4 left-9 w-[40rem]  -translate-y-1/2">
        <div class="mb-5 text-6xl text-black title-home-dative">DATIVE</div>
        <div>
          LEVIER DE
          TRANSFORMATION DIGITALE,
        </div>
        <div>
          PAR ET POUR L’INDUSTRIE
        </div>
      </div>

      <ProductionLine class="absolute left-2/3 top-[55%]  h-[30rem] w-[50rem] -translate-y-1/2 -translate-x-1/2" />

    </Section>

    <Section :top-left="0"
      :top-right="40"
      :bottom-left="0"
      :bottom-right="5"
      class="gradient-home-02"
      style="height: 70px;" />
  </div>
</template>