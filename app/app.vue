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
	gsap.fromTo("#ssvg",{
		opacity: 0,
		y: 50
	},{
		opacity: 1,
		y: 0,
		duration: 4,
		delay: 1,
		ease: 'power4',
		scrollTrigger: {
			trigger: "#ssvg",
		}
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
		delay: 0.5,
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
		delay: 1,
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
		delay: 1.5,
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
		delay: 2,
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
	gsap.fromTo("#s1",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 0.25,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s1",
		}
	});
	gsap.fromTo("#s2",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 0.5,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s2",
		}
	});
	gsap.fromTo("#s3",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 0.75,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s3",
		}
	});
	gsap.fromTo("#s4",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 1,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s4",
		}
	});
	gsap.fromTo("#s5",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 1.25,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s5",
		}
	});
	gsap.fromTo("#s6",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 1.5,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s6",
		}
	});
	gsap.fromTo("#s7",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 1.75,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s7",
		}
	});
	gsap.fromTo("#s8",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 2,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s8",
		}
	});
	gsap.fromTo("#s9",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 2.25,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s9",
		}
	});
	gsap.fromTo("#s10",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 2.5,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s10",
		}
	});
	gsap.fromTo("#s11",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 2.75,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s11",
		}
	});
	gsap.fromTo("#s12",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 3,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s12",
		}
	});
	gsap.fromTo("#s13",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 3.25,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s13",
		}
	});
	gsap.fromTo("#s14",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 3.5,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s14",
		}
	});
	gsap.fromTo("#s15",{
		opacity: 0,
		y: 30
	},{
		opacity: 1,
		y: 0,
		duration: 1,
		delay: 4,
		ease: 'power3',
		scrollTrigger: {
			trigger: "#s15",
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
</style>
