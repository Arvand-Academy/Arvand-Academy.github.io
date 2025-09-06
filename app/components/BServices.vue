<template>
  <section id="services" class="w-full min-h-svh flex flex-col md:flex-row justify-around items-center px-4 mt-2">
    <div>
    <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 md:w-64 md:h-64" viewBox="0 0 24 24" id="ssvg">
      <!-- Icon from Huge Icons by Hugeicons - undefined -->
      <path fill="currentColor" fill-rule="evenodd" d="M11.95 2.5h.1c.9 0 1.65 0 2.24.08c.63.08 1.19.27 1.65.73c.46.45.64 1.02.73 1.65c.06.43.07.95.08 1.55c.61.01 1.14.03 1.61.08c.89.09 1.63.28 2.28.71c.52.35.96.79 1.31 1.31c.43.65.62 1.39.71 2.28c.09.86.09 1.95.09 3.32v.08c0 1.37 0 2.46-.09 3.32c-.09.89-.28 1.63-.71 2.28c-.35.52-.79.96-1.31 1.31c-.65.43-1.39.62-2.28.71c-.87.09-1.95.09-3.32.09H8.96c-1.37 0-2.45 0-3.32-.09c-.89-.09-1.63-.28-2.28-.71c-.52-.35-.96-.79-1.31-1.31c-.43-.65-.62-1.39-.71-2.28c-.09-.86-.09-1.95-.09-3.32v-.08c0-1.37 0-2.46.09-3.32c.09-.89.28-1.63.71-2.28c.35-.52.79-.96 1.31-1.31c.65-.43 1.39-.62 2.28-.71c.47-.05 1-.07 1.61-.08c0-.6.02-1.12.08-1.55c.08-.63.27-1.2.73-1.65c.46-.46 1.02-.65 1.65-.73c.59-.08 1.34-.08 2.24-.08m3.23 2.66c.05.34.06.77.06 1.34h-6.5c0-.57.02-1 .06-1.34c.06-.47.17-.66.3-.79s.33-.24.79-.3C10.37 4 11.02 4 11.98 4s1.61 0 2.09.07c.46.06.66.17.79.3s.24.32.3.79zM5.79 8.08c-.77.08-1.23.23-1.6.47c-.35.23-.66.54-.9.89c-.24.37-.39.83-.47 1.6c-.08.78-.08 1.79-.08 3.21s0 2.43.08 3.21c.08.77.23 1.23.47 1.6c.24.35.54.66.9.89c.36.24.83.39 1.6.47c.78.08 1.79.08 3.21.08h6c1.42 0 2.43 0 3.21-.08c.77-.08 1.23-.23 1.6-.47c.35-.23.66-.54.9-.89c.24-.37.39-.83.47-1.6c.08-.78.08-1.79.08-3.21s0-2.43-.08-3.21c-.08-.77-.23-1.23-.47-1.6c-.24-.35-.54-.66-.9-.89c-.36-.24-.83-.39-1.6-.47C17.43 8 16.42 8 15 8H9c-1.42 0-2.43 0-3.21.08m.43 2.45a.75.75 0 0 0-.94.5c-.12.39.1.81.49.94l.65.2c1.55.48 3.18.75 4.82.82v1.26c0 .41.34.75.75.75s.75-.34.75-.75v-1.26c1.64-.07 3.27-.34 4.82-.82l.65-.2c.4-.13.62-.55.49-.94a.75.75 0 0 0-.94-.5l-.65.21a17.7 17.7 0 0 1-10.25 0l-.65-.21z" color="currentColor"/>
    </svg>
    </div>
    <div class="text-lg lg:text-xl text-center md:mt-2">
      <ul class="grid grid-cols-1 lg:grid-cols-2 gap-2 text-white dark:text-black items-end">
        <li class="mb-2 text-black dark:text-white"><h3 class="text-3xl uppercase">{{ $t('services')  }}</h3></li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s1">{{ $t('s1')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s2">{{ $t('s2')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s3">{{ $t('s3')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s4">{{ $t('s4')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s5">{{ $t('s5')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s6">{{ $t('s6')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s7">{{ $t('s7')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s8">{{ $t('s8')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s9">{{ $t('s9')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s10">{{ $t('s10')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s11">{{ $t('s11')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s12">{{ $t('s12')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s13">{{ $t('s13')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s14">{{ $t('s14')  }}</li>
        <li class="bg-blue-600 dark:bg-green-400 rounded-md py-0.5 px-1" id="s15">{{ $t('s15')  }}</li>
      </ul>
    </div>
  </section>
</template>
