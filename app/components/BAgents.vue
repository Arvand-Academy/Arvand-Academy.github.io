<template>
  <section id="agents" class="w-full min-h-svh flex flex-col md:flex-row justify-around items-center px-4 mt-2">
    <div>
      <svg xmlns="http://www.w3.org/2000/svg" class="w-32 h-32 md:w-64 md:h-64" id="asvg" viewBox="0 0 24 24">
        <!-- Icon from Material Symbols by Google - https://github.com/google/material-design-icons/blob/master/LICENSE -->
        <path fill="currentColor" d="M11.875 20q.1 0 .2-.05t.15-.1l8.2-8.2q.3-.3.438-.675t.137-.75q0-.4-.137-.763t-.438-.637l-4.25-4.25q-.275-.3-.638-.437T14.776 4q-.375 0-.75.138t-.675.437l-.275.275l1.85 1.875q.375.35.55.8t.175.95q0 1.05-.712 1.763t-1.763.712q-.5 0-.962-.175t-.813-.525L9.525 8.4L5.15 12.775q-.075.075-.112.163T5 13.125q0 .2.15.363t.35.162q.1 0 .2-.05t.15-.1l2.7-2.7q.275-.275.688-.288t.712.288q.275.275.275.7t-.275.7l-2.675 2.7q-.075.075-.112.163t-.038.187q0 .2.15.35t.35.15q.1 0 .2-.05t.15-.1l2.7-2.675q.275-.275.688-.288t.712.288q.275.275.275.7t-.275.7l-2.675 2.7q-.075.05-.112.15t-.038.2q0 .2.15.35t.35.15q.1 0 .188-.038t.162-.112l2.7-2.675q.275-.275.688-.288t.712.288q.275.275.275.7t-.275.7l-2.7 2.7q-.075.075-.112.163t-.038.187q0 .2.163.35t.362.15m-.025 2q-.925 0-1.637-.612t-.838-1.538q-.85-.125-1.425-.7t-.7-1.425q-.85-.125-1.412-.712T5.15 15.6q-.95-.125-1.55-.825t-.6-1.65q0-.5.188-.962t.537-.813L8.1 6.975Q8.675 6.4 9.513 6.4t1.412.575L12.8 8.85q.05.075.15.113t.2.037q.225 0 .375-.137t.15-.363q0-.1-.038-.2t-.112-.15L9.95 4.575q-.275-.3-.637-.437T8.55 4q-.375 0-.75.138t-.675.437L3.6 8.125q-.35.35-.5.825t-.075.95q.075.425-.175.75t-.675.375t-.75-.188t-.375-.662q-.15-.95.138-1.862T2.175 6.7L5.7 3.175Q6.3 2.6 7.038 2.3T8.55 2t1.513.3t1.312.875l.275.275l.275-.275q.6-.575 1.338-.875t1.512-.3t1.513.3t1.312.875L21.825 7.4q.575.575.875 1.325t.3 1.525t-.3 1.513t-.875 1.312l-8.2 8.175q-.35.35-.812.55t-.963.2M9.4 8"/>
      </svg>
    </div>
    <div class="max-w-128 text-lg sm:text-xl text-center md:mt-2">
      <ul class="flex flex-col gap-1">
        <li class="mb-2"><h3 class="text-3xl uppercase bg-blue-600 text-white dark:bg-green-400 dark:text-black py-1 px-2 rounded-md">{{ $t('agents')  }}</h3></li>
        <li id="i1" class="px-3 py-2 rounded-md bg-black/5 dark:bg-white/5 border-2 border-blue-600 dark:border-green-400 transition-all duration-700 hover:px-4 hover:py-3 group">
          <img src="/fardad.png" class="w-64 rounded-md grayscale-100 hover:grayscale-0 transition-all duration-700 cursor-pointer">
          <p class="mt-2 text-[0px] transition-all duration-700 group-hover:text-base">{{ $t('fardad')  }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>
