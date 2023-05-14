<template>
  <header class="menu-header">
    <nav>
      <ul>
        <li v-for="item in props.menuItems" :key="item.id" class="menu-item">
          <a :href="item.link">{{ item.label }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
const props = defineProps({
  menuItems: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped>
.menu-header {
  background-color: #f0f0f0;
  padding: 10px;
}

.menu-item {
  display: inline-block;
  margin-right: 10px;
}

.menu-item a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}
</style>
