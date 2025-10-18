<template>
    <div class="grid grid-cols-1 justify-items-stretch">
        <div class="px-2">
            <div class="text-4xl sm:text-4xl md:text-6xl lg:text-8xl text-center relative">
                <h1 class="bg-clip-text text-transparent bg-linear-180 from-violet-700 to-black">{{ $t('name') }}</h1>
            </div>
        </div>
        <div
            class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-5 gap-2 mt-8 px-5 text-center justify-items-center justify-center items-center text-xl">
            <NuxtLink v-for="item in links"
                class="bg-neutral-900/10 w-full sm:w-fit cursor-pointer px-6 py-4 shadow rounded-xl translate-y-1 hover:translate-y-0 hover:bg-violet-600 hover:text-white backdrop-blur-xs transition-all duration-300"
                :to="`/${item}`">{{
                    $t(item) }}</NuxtLink>
            <div class="w-full sm:w-fit">
                <button
                class="bg-neutral-900/10 w-full sm:w-fit cursor-pointer px-6 py-4 shadow rounded-xl translate-y-1 hover:translate-y-0 hover:bg-violet-600 hover:text-white backdrop-blur-xs transition-all duration-300"
                    v-show="currentlang == 'en'" @click="changelang('fa')">Fa</button>
                <button
                class="bg-neutral-900/10 w-full sm:w-fit cursor-pointer px-6 py-4 shadow rounded-xl translate-y-1 hover:translate-y-0 hover:bg-violet-600 hover:text-white backdrop-blur-xs transition-all duration-300"
                    v-show="currentlang == 'fa'" @click="changelang('en')">En</button>
            </div>
        </div>
    </div>
</template>
<script setup>
const links = ['about', 'contact', 'services', 'agents']
const { setLocale, locale } = useI18n()
const currentlang = ref(locale.value)
const changelang = async (lang) => {
    try {
        await setLocale(lang);
    } catch (e) {
        console.error('Error:', e)
    }
    currentlang.value = locale.value;
}
</script>