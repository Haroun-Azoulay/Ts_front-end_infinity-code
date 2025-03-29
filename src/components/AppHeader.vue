<template>
  <header class="bg-white">
    <nav
      class="mx-auto max-w-7xl items-center flex justify-between p-6 lg:px-8"
      aria-label="Global"
    >
      <div class="flex">
        <a href="#" class="m-1.5 p-1.5">
          <!-- Logo about my company. -->
          <img
class="w-30 h-20 sm:w-40 sm:h-24 md:w-52 md:h-32 lg:w-60 lg:h-36 xl:w-64 xl:h-40 2xl:w-72 2xl:h-48 mx-auto mt-4"
            src="../assets/logo_infinityCode.png"
            alt="Logo Infinity Code"
          />
        </a>
      </div>
      <div class="flex lg:hidden ml-auto items-center">
        <button type="button" class="inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
          <span class="sr-only">Open main menu</span>
          <Bars3Icon class="size-10 md:size-12 text-blue-900" aria-hidden="true" />
        </button>
      </div>
      <PopoverGroup class="hidden lg:flex lg:gap-x-12 items-center justify-center">
        <div class="lg:flex lg:gap-x-12 items-center">
          <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Accueil</A>
          <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Qui suis-je ?</a>
          <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Contact</a>
        </div>
      </PopoverGroup>
      <div class="flex">
        <button class="hidden lg:inline-block bg-gradient-to-bl from-blue-700 to-blue-900 hover:scale-105 transition-transform text-white font-bold px-7 py-2 rounded-full">
          Rendez-vous gratuit
        </button>
      </div>
    </nav>
    <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
      <div class="fixed inset-0 z-10" />
      <DialogPanel class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
        <div class="flex items-center justify-between">
          <a href="#" class="-m-1.5 p-1.5">
            <img class="w-30 h-20" src="../assets/logo_infinityCode.png" alt="Logo Infinity Code">
          </a>
          <button type="button" class="m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
            <span class="sr-only">Close menu</span>
            <XMarkIcon class="size-12 text-blue-900" aria-hidden="true" />
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/10">
            <div class="space-y-2 py-6">
              <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold  hover:text-blue-900">Accueil</a>
              <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold  hover:text-blue-900">Qui suis-je ?</a>
              <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold  hover:text-blue-900">Contact</a>
              <button class="mt-3 bg-gradient-to-bl from-blue-700 to-blue-900 hover:scale-105 transition-transform text-white font-bold px-7 py-2 rounded-full">
          Rendez-vous gratuit
        </button>
            </div>
          </div>
        </div>
      </DialogPanel>
    </Dialog>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import {
  Dialog,
  DialogPanel,
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
} from '@headlessui/vue'
import {
  ArrowPathIcon,
  Bars3Icon,
  ChartPieIcon,
  CursorArrowRaysIcon,
  FingerPrintIcon,
  SquaresPlusIcon,
  XMarkIcon,
} from '@heroicons/vue/24/outline'
const mobileMenuOpen = ref(false)
</script>
