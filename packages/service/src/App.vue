<template>
  <div>
    <MenuHeader :menu-items="MENU_ITEMS" />
    <Checkbox />
  </div>
</template>

<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import { MenuHeader } from "@gc/shares";
import { Checkbox } from "@gc/ui";

const MENU_ITEMS = [
  {
    id: 1,
    label: "Home",
    link: "/",
  },
  {
    id: 2,
    label: "About",
    link: "/about",
  },
  {
    id: 3,
    label: "Contact",
    link: "/contact",
  },
];
</script>
