<template>
	<div>
		<div
			class="flex flex-col justify-center items-center bg-[color:hsl(0,0%,90%)] dark:bg-[color:hsl(0,0%,0%)] text-[color:hsl(0,0%,5%)] dark:text-[color:hsl(0,0%,95%)] min-h-svh w-full relative vazir">
			<MainMenu />
			<main class="w-full min-h-svh">
				<div class="h-[2px] w-full bg-gradient-to-r from-transparent via-blue-600 dark:via-green-400 to-transparent"></div>
				<BHome />
			</main>
		</div>
	</div>
</template>
<script setup>
import { gsap } from 'gsap';
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { SplitText  } from 'gsap/SplitText';
import DrawSVGPlugin from 'gsap/DrawSVGPlugin'
import MainMenu from './components/MainMenu.vue';
import BHome from './components/BHome.vue';
gsap.registerPlugin(ScrollTrigger, DrawSVGPlugin);
const { t, locale, setLocale } = useI18n();
const i18nHead = useLocaleHead({ addSeoAttributes: true, addDirAttribute: true });
const pageTitle = computed(() => t('name'));
useHead({
	title: pageTitle,
	htmlAttrs: {
		lang: i18nHead.value.htmlAttrs.lang,
		dir: i18nHead.value.htmlAttrs.dir,
		class: 'scroll-smooth',
	}
});
watch(locale, () => {
	useHead({
		title: t('name'),
		htmlAttrs: {
			lang: i18nHead.value.htmlAttrs.lang,
			dir: i18nHead.value.htmlAttrs.dir,
		},
	});
});
onMounted(()=>{
	const mainsize = ()=>{
		document.documentElement.style.setProperty('--menu', document.querySelector("menu").offsetHeight + 2 + "px");
		document.querySelector("main").style.paddingTop =  document.querySelector("menu").offsetHeight + "px";
	}
	window.addEventListener("resize",()=>{
		mainsize();		
	});
	mainsize();
	let btitle = new SplitText("menu h1", { type: "chars" });
	gsap.from(btitle.chars, {
  	duration: 0.5,
  	scale: "random(0,5)",
		y: "random(-100,100)",
		x: "random(-100,100)",
		rotate: "random(360,-360)",
  	autoAlpha: 0,
  	stagger: 0.2,
		onComplete: () => { btitle.revert()  }
	});
	gsap.from('#tsvg path:nth-child(1)',{
		drawSVG: '0%',
		duration: 6,
		delay: 1.5,
		ease: 'power2'
	});
	gsap.from('#tsvg path:nth-child(2)',{
		drawSVG: '0%',
		duration: 6,
		delay: 2.5,
		ease: 'power4'
	});
});
</script>
<style>
.v-enter-active,
.v-leave-active {
	transition: all 0.3s ease-in-out;
}

.v-enter-from,
.v-leave-to {
	transform: translateY(80px);
	opacity: 0;
}
</style>
