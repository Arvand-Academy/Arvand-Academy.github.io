<template>
    <div class="grid grid-cols-1 justify-items-stretch">
        <div class="flex gap-x-5 items-center justify-center">
            <h1 class="text-8xl font-bold text-shadow-md text-shadow-green-500 text-center">{{ $t('name') }}</h1>
            <div class="flex justify-center mt-2">
                <button
                    class="p-4 border-2 border-white text-5xl rounded-xl backdrop-blur-xs cursor-pointer bg-black/10 backdrop-brightness-200"
                    v-if="currentlang == 'en'" @click="changelang('fa')">Fa</button>
                <button
                    class="p-4 border-2 border-white text-5xl rounded-xl backdrop-blur-xs cursor-pointer bg-black/10 backdrop-brightness-200"
                    v-if="currentlang == 'fa'" @click="changelang('en')">En</button>
            </div>
        </div>
        <div class="flex justify-between px-4 mt-6 gap-x-6 text-xl items-center flex-wrap">
            <NuxtLink
                class="px-6 py-4 rounded-xl bg-white/10 backdrop-blur-xs cursor-pointer hover:bg-black/10 backdrop-brightness-200 transition-colors duration-500"
                to="/about">{{
                    $t('about') }}</NuxtLink>
            <NuxtLink
                class="px-6 py-4 rounded-xl bg-white/10 backdrop-blur-xs cursor-pointer hover:bg-black/10 backdrop-brightness-200 transition-colors duration-500"
                to="/contact">{{
                    $t('contact') }}</NuxtLink>
            <NuxtLink
                class="px-6 py-4 rounded-xl bg-white/10 backdrop-blur-xs cursor-pointer hover:bg-black/10 backdrop-brightness-200 transition-colors duration-500"
                to="/services">{{
                    $t('services') }}</NuxtLink>
            <NuxtLink
                class="px-6 py-4 rounded-xl bg-white/10 backdrop-blur-xs cursor-pointer hover:bg-black/10 backdrop-brightness-200 transition-colors duration-500"
                to="/agents">{{
                    $t('agents') }}</NuxtLink>
        </div>
    </div>
</template>
<script setup>
const { setLocale, locale } = useI18n();
const currentlang = ref(locale.value);
const changelang = async (lang) => {
    try {
        await setLocale(lang);
    } catch (e) {
        console.error('Error:', e)
    }
    currentlang.value = locale.value;
}
</script>