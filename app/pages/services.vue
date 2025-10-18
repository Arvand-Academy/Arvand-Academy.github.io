<template>
    <section class="w-full min-h-svh flex flex-col justify-center items-center px-4 py-6">
        <div class="text-lg lg:text-xl text-center grid grid-cols-1 lg:grid-cols-2 w-full gap-5">
            <div class="w-full flex flex-col justify-center items-center">
                <h3 class="w-full bg-violet-500 text-white mb-2 py-3 px-4 rounded-xl">{{ $t('s7') }}</h3>
                <ul
                    class="bg-neutral-900/10 w-full backdrop-blur-xs rounded-xl py-4 px-2 h-full flex flex-col justify-around items-center">
                    <li class="py-1 px-2">{{ $t('s8') }}</li>
                    <li class="py-1 px-2">{{ $t('s9') }}</li>
                    <li class="py-1 px-2">{{ $t('s10') }}</li>
                    <li class="py-1 px-2">{{ $t('s11') }}</li>
                    <li class="py-1 px-2">{{ $t('s12') }}</li>
                    <li class="py-1 px-2">{{ $t('s13') }}</li>
                    <li class="py-1 px-2">{{ $t('s14') }}</li>
                    <li class="py-1 px-2">{{ $t('s15') }}</li>
                </ul>
            </div>
            <div class="w-full flex flex-col gap-y-4 h-fit justify-between items-center">
                <div class="w-full flex flex-col justify-center items-center">
                    <h3 class="w-full bg-violet-500 text-white mb-2 py-3 px-4 rounded-xl">{{ $t('s1') }}</h3>
                    <ul
                        class="bg-neutral-900/10 w-full backdrop-blur-xs rounded-xl py-4 px-2 h-full flex flex-col justify-around items-center">
                        <li class="py-1 px-2">{{ $t('s2') }}</li>
                        <li class="py-1 px-2">{{ $t('s3') }}</li>
                        <li class="py-1 px-2">{{ $t('s4') }}</li>
                        <li class="py-1 px-2">{{ $t('s5') }}</li>
                        <li class="py-1 px-2">{{ $t('s6') }}</li>
                    </ul>
                </div>
                <div class="w-full flex flex-col justify-center items-center">
                    <h3 class="w-full bg-violet-500 text-white mb-2 py-3 px-4 rounded-xl">{{ $t('s16') }}</h3>
                    <ul
                        class="bg-neutral-900/10 w-full backdrop-blur-xs rounded-xl py-4 px-2 h-full flex flex-col justify-around items-center">
                        <li class="py-1 px-2">{{ $t('s17') }}</li>
                        <li class="py-1 px-2">{{ $t('s18') }}</li>
                        <li class="py-1 px-2">{{ $t('s19') }}</li>
                        <li class="py-1 px-2">{{ $t('s20') }}</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="px-4 py-6 w-full flex justify-center items-center">
            <NuxtLink
                class="py-4 px-6 w-fit backdrop-blur-xs transition-colors duration-300 hover:bg-violet-600 hover:text-white text-xl text-center rounded-xl block bg-neutral-900/10"
                to="/">
                {{ $t('back') }}
            </NuxtLink>
        </div>
    </section>
</template>
<script setup>
useHead({
    title: $t('name') + ' - ' + $t('services')
})
</script>