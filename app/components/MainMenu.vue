<template>
	<menu
		class="w-full px-4 py-6 bg-white/50 dark:bg-black/50 flex flex-wrap justify-between items-center fixed top-0 left-0 z-50">
		<h1 class="text-lg md:text-xl tracking-widest">{{ $t('name') }}</h1>
		<Transition>
			<ul class="grid md:flex gap-8 justify-center justify-items-center rounded-t-lg md:justify-between items-center px-2 fixed md:relative bottom-0 bg-[color:hsl(0,0%,95%)] dark:bg-[color:hsl(0,0%,5%)]  backdrop-blur-2xl md:bg-transparent md:dark:bg-transparent right-0 w-full md:w-fit grid-cols-2 py-4 md:py-0 z-20"
				v-if="menu">
				<li @click="scrolldown('home')"
					class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{ $t('home')
					}}</li>
				<li @click="scrolldown('services')"
					class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{
						$t('services')
					}}</li>
				<li @click="scrolldown('contact')"
					class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{
						$t('contact')
					}}</li>
				<li @click="scrolldown('agents')"
					class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{
						$t('agents')
					}}</li>
				<li class="bg-slate-950/30 dark:bg-slate-50/30 h-10 w-px hidden md:block"></li>
				<li class="cursor-pointer">
					<Transition mode="out-in" name="theme">
						<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24"
							v-if="theme == 'dark'" @click="changetheme('light')">
							<!-- Icon from Huge Icons by Hugeicons - undefined -->
							<path
								class="transition-colors fill-transparent stroke-[1.5] w-6 h-6 stroke-current hover:stroke-blue-600 dark:hover:stroke-green-400"
								d="M17 12a5 5 0 1 1-10 0a5 5 0 0 1 10 0M12 2c-.377.333-.905 1.2 0 2m0 16c.377.333.906 1.2 0 2m7.5-17.497c-.532-.033-1.575.22-1.496 1.495M5.496 17.5c.033.532-.22 1.575-1.496 1.496M5.003 4.5c-.033.532.22 1.576 1.497 1.497M18 17.503c.532-.032 1.575.208 1.496 1.414M22 12c-.333-.377-1.2-.905-2 0m-16-.5c-.333.377-1.2.906-2 0"
								color="currentColor" />
						</svg>
						<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24"
							v-else-if="theme == 'light'" @click="changetheme('dark')">
							<!-- Icon from Huge Icons by Hugeicons - undefined -->
							<path
								class="transition-colors fill-transparent stroke-[1.5] w-6 h-6 stroke-current hover:stroke-blue-600 dark:hover:stroke-green-400"
								d="M21.5 14.078A8.557 8.557 0 0 1 9.922 2.5C5.668 3.497 2.5 7.315 2.5 11.873a9.627 9.627 0 0 0 9.627 9.627c4.558 0 8.376-3.168 9.373-7.422"
								color="currentColor" />
						</svg>
					</Transition>
				</li>
				<li class="text-lg">
					<button class="cursor-pointer hover:text-blue-600 dark:hover:text-green-400 transition-colors"
						v-if="currentlang == 'en'" @click="changelang('fa')">Fa</button>
					<button class="cursor-pointer hover:text-blue-600 dark:hover:text-green-400 transition-colors"
						v-if="currentlang == 'fa'" @click="changelang('en')">En</button>
				</li>
			</ul>
		</Transition>
		<button @click="togglemenu()" class="block md:hidden">
			<svg xmlns="http://www.w3.org/2000/svg"
				class="transition-colors fill-current w-6 h-6 hover:fill-blue-600 dark:hover:fill-green-400 cursor-pointer"
				viewBox="0 0 16 16">
				<path
					d="M1 2.5A1.5 1.5 0 0 1 2.5 1h3A1.5 1.5 0 0 1 7 2.5v3A1.5 1.5 0 0 1 5.5 7h-3A1.5 1.5 0 0 1 1 5.5zM2.5 2a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zm6.5.5A1.5 1.5 0 0 1 10.5 1h3A1.5 1.5 0 0 1 15 2.5v3A1.5 1.5 0 0 1 13.5 7h-3A1.5 1.5 0 0 1 9 5.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zM1 10.5A1.5 1.5 0 0 1 2.5 9h3A1.5 1.5 0 0 1 7 10.5v3A1.5 1.5 0 0 1 5.5 15h-3A1.5 1.5 0 0 1 1 13.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zm6.5.5A1.5 1.5 0 0 1 10.5 9h3a1.5 1.5 0 0 1 1.5 1.5v3a1.5 1.5 0 0 1-1.5 1.5h-3A1.5 1.5 0 0 1 9 13.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5z" />
			</svg>
		</button>
	</menu>
</template>
<script setup>
import { useI18n } from 'vue-i18n';
import { gsap } from 'gsap';
import { ScrollToPlugin } from "gsap/ScrollToPlugin";
gsap.registerPlugin(ScrollToPlugin);
const { t, locale, setLocale } = useI18n();
const menu = ref(true);
const theme = ref("");
const currentlang = ref(locale.value);
const togglemenu = () => {
	menu.value = !menu.value;
}
const menuscreensize = () => {
	if (window.innerWidth < 768) {
		menu.value = false;
	} else {
		menu.value = true;
	}
}
const scrolldown = (e) => {
	gsap.to(window, {
		duration: 0,
		scrollTo: document.querySelector("#" + e),
	});
}
const changelang = async (lang) => {
	try {
		await setLocale(lang);
	} catch (e) {
		console.error('Error:', e)
	}
	currentlang.value = locale.value;
}
const loadTheme = () => {
	document.documentElement.classList.toggle(
		"dark",
		localStorage.theme === "dark" ||
		(!("theme" in localStorage) && window.matchMedia("(prefers-color-scheme: dark)").matches),
	);
	theme.value = localStorage.theme;
}
const changetheme = (key) => {
	localStorage.theme = key;
	loadTheme();
}
onMounted(() => {
	if (!localStorage.theme) {
		changetheme('dark');
	}
	loadTheme();
	menuscreensize();
	window.addEventListener("resize", menuscreensize);
});
</script>
