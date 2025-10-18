<template>
	<div class="bg-neutral-200 min-h-svh w-full text-black vazir">
		<div class="dot-grid-container">
			<DotGrid :dot-size="5" :gap="20" base-color="#d4d4d4" active-color="#8e51ff" :proximity="150"
				:speed-trigger="100" :shock-radius="250" :shock-strength="5" :max-speed="5000" :resistance="750"
				:return-duration="1.5" />
		</div>
		<div class="min-h-svh w-full flex flex-col justify-center items-center z-20 relative">
			<NuxtPage></NuxtPage>
		</div>
	</div>
</template>
<script setup>
import DotGrid from "./DotGrid.vue";
const { t, locale } = useI18n();
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
</script>
<style>
.dot-grid-container {
	width: 100%;
	height: 100svh;
	position: fixed;
	top: 0;
	left: 0;
	overflow: hidden;
	z-index: 10;
}
</style>