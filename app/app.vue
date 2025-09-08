<template>
	<div>
		<div
			class="flex flex-col justify-center items-center bg-[color:hsl(0,0%,90%)] dark:bg-[color:hsl(0,0%,0%)] text-[color:hsl(0,0%,5%)] dark:text-[color:hsl(0,0%,95%)] min-h-svh w-full relative vazir">
			<MainMenu />
			<main class="w-full min-h-svh">
				<div class="h-[2px] w-full bg-gradient-to-r from-transparent via-blue-600 dark:via-green-400 to-transparent"></div>
				<BHome />
				<BServices />
				<BContact />
				<BAgents />
				<div class="w-full text-center text-black/10 dark:text-white/10 py-1"><a href="//imdanieldev.github.io" target="_blank">{{ $t('devmsg')  }}</a></div>
			</main>
		</div>
	</div>
</template>
<script setup>
import { gsap } from 'gsap';
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { SplitText  } from 'gsap/SplitText';
import MainMenu from './components/MainMenu.vue';
import BHome from './components/BHome.vue';
import BServices from './components/BServices.vue';
import BContact from './components/BContact.vue';
import BAgents from './components/BAgents.vue';
gsap.registerPlugin(ScrollTrigger , SplitText);
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
	gsap.fromTo("#ccsvg",{
		opacity: 0,
		y: 50
	},{
		opacity: 1,
		y: 0,
		duration: 4,
		delay: 1,
		ease: 'power4',
		scrollTrigger: {
			trigger: "#ccsvg",
		}
	});
	gsap.fromTo("#asvg",{
		opacity: 0,
		y: 50
	},{
		opacity: 1,
		y: 0,
		duration: 4,
		delay: 1,
		ease: 'power4',
		scrollTrigger: {
			trigger: "#asvg",
		}
	});
	gsap.fromTo("#desc",{
		opacity: 0,
		y: 50
	},{
		opacity: 1,
		y: 0,
		duration: 4,
		delay: 1,
		ease: 'power4',
	});
	gsap.fromTo("#c1",{
		scale: 0
	},{
		scale: 1,
		duration: 1,
		delay: 0,
		ease: 'bounce',
		scrollTrigger: {
			trigger: "#c1",
		}
	});
	gsap.fromTo("#c2",{
		scale: 0
	},{
		scale: 1,
		duration: 1,
		delay: 0.5,
		ease: 'bounce',
		scrollTrigger: {
			trigger: "#c2",
		}
	});
	gsap.fromTo("#c3",{
		scale: 0
	},{
		scale: 1,
		duration: 1,
		delay: 1,
		ease: 'bounce',
		scrollTrigger: {
			trigger: "#c3",
		}
	});
	gsap.fromTo("#c4",{
		scale: 0
	},{
		scale: 1,
		duration: 1,
		delay: 1.5,
		ease: 'bounce',
		scrollTrigger: {
			trigger: "#c4",
		}
	});
	gsap.fromTo("#i1",{
		opacity: 0,
		y: 50
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 1,
		ease: 'power4',
		scrollTrigger: {
			trigger: "#i1",
		}
	});
	gsap.from('#tsvg path',
	{
		y: -5,
		x: 10,
		rotate: -180,
		opacity: 0,
		duration: 4,
		delay: 1,
		ease: 'power2',
	});
	gsap.from('#bsvg path',
	{
		y: -5,
		x: -10,
		opacity: 0,
		rotate: 180,
		duration: 5,
		delay: 1,
		ease: 'power1',
	});
	gsap.from('#msvg path',
	{
		y: 5,
		x: -5,
		opacity: 0,
		rotate: 90,
		duration: 6,
		delay: 1,
		ease: 'power3',
	});
	gsap.from('#dsvg path',
	{
		opacity: 0,
		y: 10,
		x: 20,
		rotate: -90,
		duration: 4,
		delay: 1,
		ease: 'power4',
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

.theme-enter-active,
.theme-leave-active {
	transition: all 0.2s ease-in-out;
}

.theme-enter-from,
.theme-leave-to {
	transform: rotate(360deg);
	opacity: 0;
}
</style>
