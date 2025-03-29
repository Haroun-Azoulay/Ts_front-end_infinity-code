<template>
  <header class="bg-white">
    <nav
      class="mx-auto max-w-7xl items-center justify-between p-6 lg:px-8 lg:flex"
      aria-label="Global"
    >
      <div class="flex">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">Your Company</span>
          <!-- Logo about my company. -->
          <img
            class="mt-4 w-96 size-40"
            src="../assets/logo_infinityCode.png"
            alt=""
          />
        </a>
      </div>
      <PopoverGroup class="hidden lg:flex lg:gap-x-12 items-center justify-center">
        <div class="lg:flex lg:gap-x-12 items-center">
        <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Accueil</A>
        <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Qui suis-je ?</a>
        <a href="#" class="font-semibold text-gray-900 hover:text-blue-900 text-xl">Contact</a>
          </div>
             </PopoverGroup>
       <div class="flex">
             <button class="bg-linear-to-bl from-blue-700 to-blue-900 hover:scale-105 text-white font-bold px-7 py-2 rounded-full">
  Rendez-vous gratuit
</button>

          </div>

         </nav>

  </header>
</template>

<script setup>
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
import { ChevronDownIcon, PhoneIcon, PlayCircleIcon } from '@heroicons/vue/20/solid'

const products = [
  {
    name: 'Analytics',
    description: 'Get a better understanding of your traffic',
    href: '#',
    icon: ChartPieIcon,
  },
  {
    name: 'Engagement',
    description: 'Speak directly to your customers',
    href: '#',
    icon: CursorArrowRaysIcon,
  },
  {
    name: 'Security',
    description: 'Your customers’ data will be safe and secure',
    href: '#',
    icon: FingerPrintIcon,
  },
  {
    name: 'Integrations',
    description: 'Connect with third-party tools',
    href: '#',
    icon: SquaresPlusIcon,
  },
  {
    name: 'Automations',
    description: 'Build strategic funnels that will convert',
    href: '#',
    icon: ArrowPathIcon,
  },
]
const callsToAction = [
  { name: 'Watch demo', href: '#', icon: PlayCircleIcon },
  { name: 'Contact sales', href: '#', icon: PhoneIcon },
]

const mobileMenuOpen = ref(false)
</script>
