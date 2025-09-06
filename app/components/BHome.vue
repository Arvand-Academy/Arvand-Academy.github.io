<template>
  <section id="home" class="w-full min-h-[calc(100svh_-_var(--menu))] flex flex-wrap flex-col md:flex-row justify-around items-center px-4 py-6 gap-5">
    <div class="grid gap-3 grid-cols-2">
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 overflow-visible" viewBox="0 0 24 24" id="bsvg">
        <!-- Icon from Huge Icons by Hugeicons - undefined -->
        <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M7 17v-4m5 4V7m5 10v-6M2.5 12c0-4.478 0-6.718 1.391-8.109S7.521 2.5 12 2.5c4.478 0 6.718 0 8.109 1.391S21.5 7.521 21.5 12c0 4.478 0 6.718-1.391 8.109S16.479 21.5 12 21.5c-4.478 0-6.718 0-8.109-1.391S2.5 16.479 2.5 12" color="currentColor"/>
      </svg>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 overflow-visible" viewBox="0 0 24 24" id="tsvg">
        <!-- Icon from Huge Icons by Hugeicons - undefined -->
        <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5.5 3v5M8 5.5H3M8 16l-2 2m0 0l-2 2m2-2l2 2m-2-2l-2-2M20 6h-4m4 12.5h-4m4-3h-4m6-3.5H2m10 10V2" color="currentColor"/>
      </svg>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 overflow-visible" viewBox="0 0 24 24" id="msvg">
        <!-- Icon from Huge Icons by Hugeicons - undefined -->
        <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor">
          <path d="M2 14c0-3.507 0-5.26.908-6.44q.25-.325.554-.592C4.57 6 6.212 6 9.5 6h5c3.288 0 4.931 0 6.038.968q.304.268.554.592C22 8.74 22 10.493 22 14s0 5.26-.908 6.44a4 4 0 0 1-.554.591C19.43 22 17.788 22 14.5 22h-5c-3.287 0-4.931 0-6.038-.968a4 4 0 0 1-.554-.592C2 19.26 2 17.507 2 14m14-8c0-1.886 0-2.828-.586-3.414S13.886 2 12 2s-2.828 0-3.414.586S8 4.114 8 6"/>
          <path d="M12 11c-1.105 0-2 .672-2 1.5s.895 1.5 2 1.5s2 .672 2 1.5s-.895 1.5-2 1.5m0-6c.87 0 1.612.417 1.886 1M12 11v-1m0 7c-.87 0-1.612-.417-1.886-1M12 17v1m-6-6H2m20 0h-4"/>
        </g>
      </svg>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 overflow-visible" viewBox="0 0 24 24" id="dsvg">
        <!-- Icon from Huge Icons by Hugeicons - undefined -->
        <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor">
          <path d="M21 21H10c-3.3 0-4.95 0-5.975-1.025S3 17.3 3 14V3m3 9h.009m2.99 0h.008m2.99 0h.008m2.99 0h.009m2.989 0h.009m2.989 0H21"/>
          <path d="M6 7c.673-1.122 1.587-2 2.993-2c5.943 0 2.602 12 8.989 12c1.416 0 2.324-.884 3.018-2"/>
        </g>
      </svg>
    </div>
    <div class="w-full md:max-w-128 text-lg sm:text-xl text-center mt-4 md:mt-0 group" id="desc">
      <h4 class="py-1 px-2 text-xl group-hover:-translate-y-3 transition-all duration-700 bg-blue-600 dark:bg-green-400 text-white dark:text-black rounded-t-md group-hover:rounded-md">{{ $t('desct')  }}</h4>
      <p class="bg-black/5 dark:bg-white/5 border-2 border-blue-600 dark:border-green-400 py-2 px-4 rounded-b-md group-hover:rounded-md transition-all duration-700 overflow-hidden relative">
        {{ $t('desc')  }}
        <div class="w-20 h-20 blur-3xl transition-all duration-700 bg-blue-800 dark:bg-green-400 absolute rounded-full group-hover:w-30 group-hover:h-30 group-hover:blur-4xl"></div>
      </p>
    </div>
    <div class="w-full md:max-w-72 text-lg sm:text-xl text-center mt-4 md:mt-0 group" id="desc">
      <h4 class="py-1 px-2 text-xl group-hover:-translate-y-3 transition-all duration-700 bg-blue-600 dark:bg-green-400 text-white dark:text-black rounded-t-md group-hover:rounded-md">{{ $t('desc2t')  }}</h4>
      <p class="bg-black/5 dark:bg-white/5 border-2 border-blue-600 dark:border-green-400 py-2 px-4 rounded-b-md group-hover:rounded-md transition-all duration-700 overflow-hidden relative">
        {{ $t('desc2')  }}
        <div class="w-20 h-20 blur-3xl transition-all duration-700 bg-blue-800 dark:bg-green-400 absolute rounded-full group-hover:w-30 group-hover:h-30 group-hover:blur-4xl"></div>
      </p>
    </div>
  </section>
</template>
