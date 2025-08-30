<template>
	<menu
		class="w-full px-4 py-6 bg-[color:hsla(0,0%,95%,0.8)] dark:bg-[color:hsla(0,0%,5%,0.8)] flex flex-wrap justify-between items-center fixed top-0 left-0">
		<h1 class="text-xl tracking-widest z-20">{{ $t('name') }}</h1>
		<Transition>
			<ul class="grid md:flex gap-8 justify-center justify-items-center rounded-t-lg md:justify-between items-center px-2 fixed md:relative bottom-0 bg-[color:hsl(0,0%,95%)] dark:bg-[color:hsl(0,0%,5%)]  backdrop-blur-2xl md:bg-transparent md:dark:bg-transparent right-0 w-full md:w-fit grid-cols-2 py-4 md:py-0 z-20"
				v-if="menu.mmenu">
				<li @click="scrolldown('home')" class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{ $t('home')
				}}</li>
				<li @click="scrolldown('about')" class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{
					$t('about')
				}}</li>
				<li @click="scrolldown('services')" class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{ $t('services')
				}}</li>
				<li @click="scrolldown('contact')" class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{ $t('contact')
				}}</li>
				<li @click="scrolldown('agents')" class="cursor-pointer transition-colors hover:text-blue-600 dark:hover:text-green-400">{{ $t('agents')
				}}</li>
				<li class="bg-slate-950/30 dark:bg-slate-50/30 h-10 w-px hidden md:block"></li>
				<li @click="togglemenu('lang')">
					<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-6 w-6">
						<g class="transition-colors fill-transparent stroke-[1.5] w-6 h-6 stroke-current hover:stroke-blue-600 dark:hover:stroke-green-400 cursor-pointer">
							<path d="M5 5.828h2.7m3.3 0H9.5m-1.8 0h1.8m-1.8 0V5m1.8.828c-.316 1.131-.98 2.201-1.736 3.141M5.836 11a19 19 0 0 0 1.928-2.03m0 0c-.385-.453-.925-1.184-1.08-1.515m1.08 1.514l1.157 1.203M13.5 19l.833-2m4.167 2l-.833-2m-3.334 0L16 13l1.667 4m-3.334 0h3.334"/><path d="M14 10V8c0-2.828 0-4.243-.879-5.121C12.243 2 10.828 2 8 2s-4.243 0-5.121.879C2 3.757 2 5.172 2 8s0 4.243.879 5.121C3.757 14 5.172 14 8 14h2"/>
							<path d="M10 16c0-2.828 0-4.243.879-5.121C11.757 10 13.172 10 16 10s4.243 0 5.121.879C22 11.757 22 13.172 22 16s0 4.243-.879 5.121C20.243 22 18.828 22 16 22s-4.243 0-5.121-.879C10 20.243 10 18.828 10 16m-6 .5c0 1.404 0 2.107.337 2.611a2 2 0 0 0 .552.552C5.393 20 6.096 20 7.5 20M20 7.5c0-1.404 0-2.107-.337-2.611a2 2 0 0 0-.552-.552C18.607 4 17.904 4 16.5 4"/>
						</g>
					</svg>
				</li>
				<li @click="togglemenu('theme')">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24">
					<path class="transition-colors fill-transparent stroke-[1.5] w-6 h-6 stroke-current hover:stroke-blue-600 dark:hover:stroke-green-400 cursor-pointer" d="M17.58 9.71a6 6 0 0 0-7.16 3.58m7.16-3.58A6 6 0 1 1 12 19.972M17.58 9.71a6 6 0 1 0-11.16 0m4 3.58A6 6 0 0 0 10 15.5c0 1.777.773 3.374 2 4.472m-1.58-6.682a6.01 6.01 0 0 1-4-3.58m0 0A6 6 0 1 0 12 19.972" color="currentColor"/>
					</svg>
				</li>
			</ul>
		</Transition>
		<button @click="togglemenu('mmenu')" class="block md:hidden">
			<svg xmlns="http://www.w3.org/2000/svg"
				class="transition-colors fill-current w-6 h-6 hover:fill-blue-600 dark:hover:fill-green-400 cursor-pointer"
				viewBox="0 0 16 16">
				<path
					d="M1 2.5A1.5 1.5 0 0 1 2.5 1h3A1.5 1.5 0 0 1 7 2.5v3A1.5 1.5 0 0 1 5.5 7h-3A1.5 1.5 0 0 1 1 5.5zM2.5 2a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zm6.5.5A1.5 1.5 0 0 1 10.5 1h3A1.5 1.5 0 0 1 15 2.5v3A1.5 1.5 0 0 1 13.5 7h-3A1.5 1.5 0 0 1 9 5.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zM1 10.5A1.5 1.5 0 0 1 2.5 9h3A1.5 1.5 0 0 1 7 10.5v3A1.5 1.5 0 0 1 5.5 15h-3A1.5 1.5 0 0 1 1 13.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5zm6.5.5A1.5 1.5 0 0 1 10.5 9h3a1.5 1.5 0 0 1 1.5 1.5v3a1.5 1.5 0 0 1-1.5 1.5h-3A1.5 1.5 0 0 1 9 13.5zm1.5-.5a.5.5 0 0 0-.5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 0-.5-.5z" />
			</svg>
		</button>
	</menu>
	<Transition>
		<div v-if="menu.lang" class="fixed bottom-4 left-1/2 w-full px-2 -translate-x-1/2 flex justify-center">
			<div
				class="bg-black/5 dark:bg-white/5 rounded-md  backdrop-blur-2xl text-black dark:text-white px-3 md:px-12 py-2 flex flex-wrap gap-2 md:gap-12 select-none w-full md:w-fit justify-around">
				<button
					class="cursor-pointer px-4 py-2 bg-slate-950/20 dark:bg-slate-50/20 rounded-sm transition-colors hover:bg-slate-950/30 dark:hover:bg-slate-50/30"
					@click="changelang('en')">{{ $t('en') }}</button>
				<button
					class="cursor-pointer px-4 py-2 bg-slate-950/20 dark:bg-slate-50/20 rounded-sm transition-colors hover:bg-slate-950/30 dark:hover:bg-slate-50/30"
					@click="changelang('fa')">{{ $t('fa') }}</button>
			</div>
		</div>
	</Transition>
	<Transition>
		<div v-if="menu.theme" class="fixed bottom-4 left-1/2 w-full px-2 -translate-x-1/2 flex justify-center">
			<div
				class="bg-slate-950/5 dark:bg-slate-50/5 rounded-md  backdrop-blur-2xl text-slate-950 dark:text-slate-50 px-3 md:px-12 py-2 flex flex-wrap gap-2 md:gap-12 select-none w-full md:w-fit justify-around">
				<button
					class="cursor-pointer px-4 py-2 bg-slate-950/20 dark:bg-slate-50/20 rounded-sm transition-colors hover:bg-slate-950/30 dark:hover:bg-slate-50/30"
					@click="changetheme('dark')">{{ $t('dark') }}</button>
				<button
					class="cursor-pointer px-4 py-2 bg-slate-950/20 dark:bg-slate-50/20 rounded-sm transition-colors hover:bg-slate-950/30 dark:hover:bg-slate-50/30"
					@click="changetheme('system')">{{ $t('system') }}</button>
				<button
					class="cursor-pointer px-4 py-2 bg-slate-950/20 dark:bg-slate-50/20 rounded-sm transition-colors hover:bg-slate-950/30 dark:hover:bg-slate-50/30"
					@click="changetheme('light')">{{ $t('light') }}</button>
			</div>
		</div>
	</Transition>
</template>
<script setup>
import { useI18n } from 'vue-i18n';
import { gsap } from 'gsap';
import { ScrollToPlugin } from "gsap/ScrollToPlugin";
gsap.registerPlugin(ScrollToPlugin);
const { t, locale, setLocale } = useI18n();
const menu = ref({
	lang: false,
	theme: false,
	mmenu: true
});
const togglemenu = (key) => {
	menu.value[key] = !menu.value[key];
	for (let skey in menu.value) {
		if (window.innerWidth < 768) {
			if (skey !== key) {
				if (menu.value['mmenu'] == true) {
					menu.value[skey] = false;
				}
			}
		} else {
			if (key == 'theme') {
				menu.value['lang'] = false;
			}
			if (key == 'lang') {
				menu.value['theme'] = false;
			}
		}
	}
}
const menuscreensize = () => {
	if (window.innerWidth < 768) {
		menu.value['mmenu'] = false;
	} else {
		menu.value['mmenu'] = true;
	}
}
const scrolldown = (e)=>{
	gsap.to(window, {
    duration: 0,
    scrollTo: document.querySelector("#"+e),
  });
}
const changelang = async (lang) => {
	try {
		await setLocale(lang);
	} catch (e) {
		console.error('Error:', e)
	}
	menu.value['lang'] = false;
}
const loadTheme = () => {
	document.documentElement.classList.toggle(
		"dark",
		localStorage.theme === "dark" ||
		(!("theme" in localStorage) && window.matchMedia("(prefers-color-scheme: dark)").matches),
	);
}
onMounted(() => {
	loadTheme();
	menuscreensize();
	window.addEventListener("resize", menuscreensize);
})
const changetheme = (key) => {
	if (key == "system") {
		localStorage.removeItem("theme");
		loadTheme()
	} else {
		localStorage.theme = key;
		loadTheme();
	}
	menu.value['theme'] = false;
}
</script>
