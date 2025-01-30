<template>
  <main class="flex flex-col sm:flex-row pt-20 min-h-screen">
    <div class="w-full sm:w-4/6 bg-[#191919] flex flex-col justify-center items-center xl:pl-32 px-6 py-16 sm:py-8">
      <div class="max-w-[420px] lg:max-w-[742px] flex flex-col items-center sm:items-start text-white text-center sm:text-left">
        <h1 class="text-3xl lg:text-7xl font-bold lg:tracking-tight">
          L’actualité simplifiée, pour aller à l’essentiel.
        </h1>
        <p class="text-xl lg:text-2xl mt-6 opacity-50">
          Grâce à l’IA, Pikor sélectionne et résume les informations clés pour que vous restiez informé, sans perdre de temps.
        </p>
        <CTA size="xl" class="mt-16"/>
      </div>
    </div>
    <div class="w-full sm:w-2/6 bg-[#454545] flex justify-center items-center px-16 sm:px-2 lg:px-16 py-16">
      <img
        class="drop-shadow-[0_35px_35px_rgba(0,0,0,0.5)]"
        src="/img/hero_smartphone.png"
        alt="hero smartphone"
        width="304"
        height="673"
      />
    </div>
  </main>
</template>
