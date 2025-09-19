<template>
  <section id="contact" class="w-full min-h-svh flex flex-col md:flex-row justify-around items-center px-4 mt-2">
      <div>
        <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 md:w-64 md:h-64" viewBox="0 0 24 24" id="ccsvg">
          <!-- Icon from Huge Icons by Hugeicons - undefined -->
          <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3.778 11.942C2.83 10.29 2.372 8.94 2.096 7.572c-.408-2.024.526-4.001 2.073-5.263c.654-.533 1.404-.35 1.791.343l.873 1.567c.692 1.242 1.038 1.862.97 2.52c-.069.659-.536 1.195-1.469 2.267zm0 0c1.919 3.346 4.93 6.36 8.28 8.28m0 0c1.653.948 3.002 1.406 4.37 1.682c2.024.408 4.001-.526 5.262-2.073c.534-.654.351-1.404-.342-1.791l-1.567-.873c-1.242-.692-1.862-1.038-2.52-.97c-.659.069-1.195.536-2.267 1.469z" color="currentColor"/>
        </svg>
      </div>
	    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-center mt-2">
        <div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group flex gap-x-1" id="c1">
		  <img src="/rahman.jpg" class="h-full w-auto">
		  <div>
          	<h4 class="text-xl md:text-2xl">{{ $t('name1')  }}</h4>
          	<p class="text-base md:text-lg">09134209635</p>
          </div>
		  <div class="bg-blue-800 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500"></div>
        </div>
        <div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group" id="c2">
          <h4 class="text-xl md:text-2xl">{{ $t('name2')  }}</h4>
          <p class="text-base md:text-lg">09162675407</p>
          <div class="bg-blue-800 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500"></div>
        </div>
        <div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group" id="c3">
          <h4 class="text-xl md:text-2xl">{{ $t('tg')  }}</h4>
          <a href="//t.me/Arvand_Financial_School" class="text-base md:text-lg break-words">@Arvand_Financial_School</a>
          <div class="bg-blue-600 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500"></div>
        </div>
        <div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group" id="c4">
          <h4 class="text-xl md:text-2xl">{{ $t('mail')  }}</h4>
          <a href="mailto:ArvandFinancialAcademy2025@gmail.com" class="text-base md:text-lg break-words">ArvandFinancialAcademy2025@gmail.com</a>
          <div class="bg-blue-600 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500"></div>
        </div>
      </div>
  </section>
</template>
