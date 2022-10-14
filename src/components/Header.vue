<template>
    <header
        class="relative flex top-0 z-50 py-7 items-center justify-between text-slate-700   leading-6 dark:text-slate-200 bg-bodyColor mx-5 xs:mx-14 lg:!mx-auto lg:max-w-5xl">

        <DarkModeToggle />

        <div class="flex items-center">
            <nav class="justify-between self-center">
              

                <div :class="menuOpen ? 'flex' : 'hidden'" class="md:flex">
                    <ul
                        class="flex flex-col absolute md:!relative right-0 2xs:right-5 top-24 py-5 rounded-lg bg-white dark:bg-slate-900 text-titleColor text-center font-semibold md:flex-row md:top-0 md:!right-0 md:space-x-8 lg:space-x-10 md:py-0 md:bg-transparent">
                        <NavLink text="Produto" link="#product" />

                        <NavLink text="Clientes" link="#clients" />

                        <NavLink text="Contrate" link="#contract" />
                    </ul>
                </div>
            </nav>

            
            <div class="flex items-center md:border-l border-slate-200 ml-6 pl-6 dark:border-slate-800">
                <DarkModeToggle />
                <button @click="menuOpen = !menuOpen" class="md:hidden ml-6 float-right cursor-pointer hover:opacity-60">
                    <Icon :icon="menuOpen ? 'ep:close-bold' : 'ep:menu'" class="text-2xl text-titleColor"
                        aria-label="menu mobile" />
                </button>
                <!-- 
            <a href="https://github.com/Ftailwindlabs/tailwindcss" class="ml-6 block text-slate-400 hover:text-slate-500 dark:hover:text-slate-300">
                <span class="sr-only">Tailwind CSS on GitHub</span>
                <svg viewBox="0 0 16 16" class="w-5 h-5"
                    fill="currentColor" aria-hidden="true">
                    <path
                        d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z">
                    </path>
                </svg>
            </a>
            -->
            </div>
        </div>


    </header>
</template>
  
<script lang="ts">
import { defineComponent } from 'vue'
import NavLink from './NavLink.vue'
import { Icon } from '@iconify/vue'
import DarkModeToggle from './DarkModeToggle.vue'

export default defineComponent({
    components: {
        NavLink,
        Icon,
        DarkModeToggle
    },
    data() {
        return {
            menuOpen: false
        }
    }
})
</script>
  