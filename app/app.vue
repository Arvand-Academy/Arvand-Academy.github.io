<template>
	<div class="bg-neutral-950 min-h-svh w-full text-white vazir">
		<div class="dot-grid-container">
			<DotGrid :dot-size="5" :gap="20" base-color="#888888" active-color="#27FF64" :proximity="120"
				:speed-trigger="100" :shock-radius="250" :shock-strength="5" :max-speed="5000" :resistance="750"
				:return-duration="1.5" class-name="custom-dot-grid" />
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
<style scoped>
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