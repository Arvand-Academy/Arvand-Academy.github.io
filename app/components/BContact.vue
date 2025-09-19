<template>
	<section id="contact" class="w-full min-h-svh flex flex-col justify-center items-center px-4 mt-2">
		<h3 class="text-2xl md:text-4xl border-blue-600 dark:border-green-400 border-b-1 w-fit">{{ $t('contact') }}
		</h3>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-center mt-4">
			<div class="bg-black/5 dark:bg-white/5 flex flex-wrap justify-between items-center rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group"
				id="c1">
				<img src="/rahman.jpg" class="w-1/3 h-full">
				<div class="w-2/3 p-3">
					<h4 class="text-lg sm:text-xl md:text-2xl">{{ $t('name1') }}</h4>
					<p class="text-base md:text-lg">09134209635</p>
				</div>
				<div
					class="bg-blue-800 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500">
				</div>
			</div>
			<div class="bg-black/5 dark:bg-white/5 flex flex-wrap justify-between items-center rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group"
				id="c2">
				<img src="/ehsan.jpg" class="w-1/3 h-full">
				<div class="w-2/3 p-3">
					<h4 class="text-lg sm:text-xl md:text-2xl">{{ $t('name1') }}</h4>
					<p class="text-base md:text-lg">09162675407</p>
				</div>
				<div
					class="bg-blue-800 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500">
				</div>
			</div>
			<div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group"
				id="c3">
				<h4 class="text-xl md:text-2xl">{{ $t('tg') }}</h4>
				<a href="//t.me/Arvand_Financial_School"
					class="text-base md:text-lg break-words">@Arvand_Financial_School</a>
				<div
					class="bg-blue-600 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500">
				</div>
			</div>
			<div class="bg-black/5 dark:bg-white/5 px-15 py-10 rounded-2xl border-2 border-blue-600 dark:border-green-400 relative overflow-hidden group"
				id="c4">
				<h4 class="text-xl md:text-2xl">{{ $t('mail') }}</h4>
				<a href="mailto:ArvandFinancialAcademy2025@gmail.com"
					class="text-base md:text-lg break-words">ArvandFinancialAcademy2025@gmail.com</a>
				<div
					class="bg-blue-600 dark:bg-green-400 w-15 h-15 rounded-full blur-2xl absolute bottom-0 right-0 group-hover:h-20 group-hover:w-20 group-hover:blur-3xl transition-all duration-500">
				</div>
			</div>
		</div>
	</section>
</template>
