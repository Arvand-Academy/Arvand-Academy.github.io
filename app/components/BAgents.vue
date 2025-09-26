<template>
  <section id="agents" class="w-full min-h-svh flex flex-col md:flex-row justify-around items-center px-4 mt-2">
    <div>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 md:w-64 md:h-64" id="asvg"
        viewBox="0 0 24 24"><!-- Icon from Huge Icons by Hugeicons - undefined -->
        <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="1.5">
          <path stroke-linejoin="round"
            d="M22 6.75h-2.789c-.601 0-.902 0-1.185-.086s-.534-.252-1.034-.586c-.75-.5-1.606-1.07-2.031-1.2c-.425-.128-.876-.128-1.778-.128c-1.226 0-2.016 0-2.568.228c-.55.229-.984.662-1.852 1.53L8 7.27c-.195.196-.293.294-.353.39a1 1 0 0 0 .062 1.149c.07.089.178.176.393.349c.796.64 1.943.576 2.664-.149L12 7.768h1l6 6.036a1.43 1.43 0 0 1 0 2.011a1.41 1.41 0 0 1-2 0l-.5-.502m-3-3.018l3 3.018m0 0a1.43 1.43 0 0 1 0 2.011a1.41 1.41 0 0 1-2 0l-1-1.006m0 0a1.43 1.43 0 0 1 0 2.012a1.41 1.41 0 0 1-2 0L10 16.821m3.5-.503l-2-2m-2 2l.5.503m0 0a1.43 1.43 0 0 1 0 2.012a1.41 1.41 0 0 1-2 0l-2.824-2.882c-.58-.592-.87-.889-1.242-1.045c-.371-.156-.786-.156-1.615-.156H2" />
          <path d="M22 14.75h-2.5m-11-8H2" />
        </g>
      </svg>
    </div>
    <div class="max-w-128 text-lg sm:text-xl text-center md:mt-2">
      <ul class="flex flex-col gap-1">
        <li class="mb-2">
          <h3 class="text-3xl uppercase bg-blue-600 text-white dark:bg-green-400 dark:text-black py-1 px-2 rounded-md">
            {{ $t('agents') }}</h3>
        </li>
        <li id="i1"
          class="px-3 py-2 rounded-md bg-black/5 dark:bg-white/5 border-2 border-blue-600 dark:border-green-400 transition-all duration-700 hover:px-4 hover:py-3 group">
          <img src="/fardad.png"
            class="w-64 rounded-md grayscale-100 hover:grayscale-0 transition-all duration-700 cursor-pointer">
          <p class="mt-2 text-[0px] transition-all duration-700 group-hover:text-base">{{ $t('fardad') }}</p>
        </li>
        <li id="i1"
          class="px-3 py-2 rounded-md bg-black/5 dark:bg-white/5 border-2 border-blue-600 dark:border-green-400 transition-all duration-700 hover:px-4 hover:py-3 group">
          <img src="/diaco.jpg"
            class="w-64 rounded-md grayscale-100 hover:grayscale-0 transition-all duration-700 cursor-pointer">
          <p class="mt-2 text-[0px] transition-all duration-700 group-hover:text-base">{{ $t('diaco') }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>
