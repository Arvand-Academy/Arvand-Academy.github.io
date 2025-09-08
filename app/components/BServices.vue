<template>
  <section id="services" class="w-full min-h-svh flex flex-col md:flex-row justify-around items-center px-4 mt-2">
    <div class="text-lg lg:text-xl text-center w-full relative flex flex-col justify-center items-center">
      <h3 class="text-2xl md:text-4xl border-blue-600 dark:border-green-400 border-b-1 w-fit">{{ $t('services')  }}</h3>
      <div class="grid grid-cols-1 items-center justify-center gap-5 mt-4">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 flex-wrap">
          <ul class="bg-white/5 rounded-md border-2 border-blue-600 dark:border-green-400 relative overflow-hidden">
            <li class="w-full bg-blue-600 text-white dark:bg-green-400 dark:text-black mb-2 py-1 px-2">{{ $t('s1')  }}</li>
            <li class="py-1 px-2">{{ $t('s2')  }}</li>
            <li class="py-1 px-2">{{ $t('s3')  }}</li>
            <li class="py-1 px-2">{{ $t('s4')  }}</li>
            <li class="py-1 px-2">{{ $t('s5')  }}</li>
            <li class="py-1 px-2">{{ $t('s6')  }}</li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute bottom-0 left-0 blur-2xl dark:blur-3xl toright"></li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute top-0 right-0 blur-2xl dark:blur-3xl toleft"></li>
          </ul>
          <ul class="bg-white/5 rounded-md border-2 border-blue-600 dark:border-green-400 relative overflow-hidden">
            <li class="w-full bg-blue-600 text-white dark:bg-green-400 dark:text-black mb-2 py-1 px-2">{{ $t('s16')  }}</li>
            <li class="py-1 px-2">{{ $t('s17')  }}</li>
            <li class="py-1 px-2">{{ $t('s18')  }}</li>
            <li class="py-1 px-2">{{ $t('s19')  }}</li>
            <li class="py-1 px-2">{{ $t('s20')  }}</li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute bottom-0 left-0 blur-2xl dark:blur-3xl toright"></li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute top-0 right-0 blur-2xl dark:blur-3xl toleft"></li>
          </ul>
        </div>
        <div>
          <ul class="bg-white/5 rounded-md border-2 border-blue-600 dark:border-green-400 relative overflow-hidden">
            <li class="w-full bg-blue-600 text-white dark:bg-green-400 dark:text-black mb-2 py-1 px-2">{{ $t('s7')  }}</li>
            <li class="py-1 px-2">{{ $t('s8')  }}</li>
            <li class="py-1 px-2">{{ $t('s9')  }}</li>
            <li class="py-1 px-2">{{ $t('s10')  }}</li>
            <li class="py-1 px-2">{{ $t('s11')  }}</li>
            <li class="py-1 px-2">{{ $t('s12')  }}</li>
            <li class="py-1 px-2">{{ $t('s13')  }}</li>
            <li class="py-1 px-2">{{ $t('s14')  }}</li>
            <li class="py-1 px-2">{{ $t('s15')  }}</li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute bottom-0 left-0 blur-2xl dark:blur-3xl toright"></li>
            <li class="p-5 rounded-full bg-blue-800 dark:bg-green-400 absolute top-0 right-0 blur-2xl dark:blur-3xl toleft"></li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.toright{
  animation: torighta 5s infinite;
}
.toleft{
  animation: tolefta 5s infinite;
}
@keyframes torighta{
  0%, 100%{
    right: 100%;
    left: 0;
    bottom: 0;
    top: 100%;
  }
  25%{
    right: 0;
    left: 100%;
    bottom: 0;
    top: 100%;
  }
  50%{
    right: 0;
    left: 100%;
    bottom: 100%;
    top: 0;
  }
  75%{
    right: 100%;
    left: 0;
    bottom: 100%;
    top: 0;
  }
}
@keyframes tolefta{
  0%, 100%{
    right: 0;
    left: 100%;
    bottom: 100%;
    top: 0;
  }
  25%{
    right: 100%;
    left: 0;
    bottom: 100%;
    top: 0;
  }
  50%{
    right: 100%;
    left: 0;
    bottom: 0;
    top: 100%;
  }
  75%{
    right: 0;
    left: 100%;
    bottom: 0;
    top: 100%;
  }
}

</style>
