<template>
  <Disclosure as="nav" class="bg-gray-800" v-slot="{ open }">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8 space-y-5 header">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <DisclosureButton
            class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
          >
            <span class="absolute -inset-0.5" />
            <span class="sr-only">Open main menu</span>
            <Bars3Icon v-if="!open" class="block h-6 w-6" aria-hidden="true" />
            <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
          </DisclosureButton>
        </div>
        <div
          class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start"
        >
          <div class="flex flex-shrink-0 items-center title-desktop">
            <span
              ><strong> Sabbat </strong>
              <span class="myName">Lumpatshia</span></span
            >
          </div>
          <div class="hidden sm:ml-6 sm:block">
            <div class="flex space-x-4 nav__menu">
              <a
                class="title-link"
                v-for="item in navigation"
                :key="item.name"
                :href="item.href"
                :class="[
                  item.current
                    ? 'bg-gray-900 text-white'
                    : 'text-gray-300 hover:bg-gray-700 hover:text-white',
                  'rounded-md px-3 py-2 text-sm font-medium',
                ]"
                :aria-current="item.current ? 'page' : undefined"
                >{{ item.name }}</a
              >
            </div>
          </div>
        </div>
        <div
          v-for="item in icones"
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0 icone-github"
        >
          <a href="https://github.com/Sabbat10" target="_blank">
            <img :src="item.github" width="45" height="40" alt="icone-github" />
          </a>
        </div>
        <div
          v-for="item in icones"
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0 icone-moon"
        >
          <a href="#" class="">
            <img :src="item.moon" width="45" height="40" alt="icone-moon" />
          </a>
        </div>
      </div>
    </div>

    <DisclosurePanel class="sm:hidden">
      <div class="space-y-1 px-2 pb-3 pt-2 title-mobile">
        <DisclosureButton
          v-for="item in navigation"
          :key="item.name"
          as="a"
          :href="item.href"
          :class="[
            item.current
              ? 'bg-gray-900 text-white'
              : 'text-gray-300 hover:bg-gray-700 hover:text-white',
            'block rounded-md px-3 py-2 text-base font-medium',
          ]"
          :aria-current="item.current ? 'page' : undefined"
          >{{ item.name }}</DisclosureButton
        >
      </div>
    </DisclosurePanel>
  </Disclosure>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { Bars3Icon, BellIcon, XMarkIcon } from "@heroicons/vue/24/outline";
import { icones } from "../../assets/Css/Data/Data";

const navigation = [
  //   { name: "Sabbat Lumpatshia", href: "#", current: true },
  { name: "Home", href: "#hiro-section", current: false, id: "hiro-section" },
  {
    name: "About",
    href: "#section-about",
    current: false,
    id: "about-section",
  },
  { name: "Work", href: "#section-work", current: false, id: "work-section" },
  {
    name: "Contact",
    href: "#section-contact",
    current: false,
    id: "contact-section",
  },
];
</script>

<style scoped>
.header {
  padding: 12px;
}
.title-desktop {
  font-size: 25.5px;
  text-align: left;
}
.title-mobile {
  font-size: 10.5px;
  color: #ffffff;
  text-align: left;
}
strong {
  font-weight: 900;
  color: #ffffff;
}
.myName {
  color: ;
}
.title-link {
  font-size: 18.5px;
}
.icone-github {
  width: 40px;
  overflow: hidden;
}
.icone-github a img {
  transition: 1s;
}
.icone-github a img:hover {
  transform: scale(1.2);
}
.icone-moon {
  width: 40px;
  overflow: hidden;
}
.icone-moon a img {
  transition: 1s;
}
.icone-moon a img:hover {
  transform: scale(1.2);
}
@media screen and (max-width: 480px) {
  .title-desktop {
    font-size: 18.5px;
    padding-right: 20px;
  }
  .icone-github {
    display: none;
  }
  .icone-moon {
    width: 40px;
    overflow: hidden;
  }
  .icone-moon a img {
    transition: 1s;
  }
}
</style>
